# NETEZZA Internal Query Processing

## Parse tree

```Text
Select  : SelectStmt
                -> targetList -> List
                                    -> ResTarget
                                            -> val |    | ------> Attr
                                                                -> relname (name of table)
                                                                -> attrs |    | -------------> Value
                                                                                                -> name of the attribute

From    :       -> fromClause -> List
                                    -> RangeVar
                                            -> name ( of_alias_)
                                            -> relExpr |    | -------> RelExpr
                                                                            -> relname( name of the table )

Where   :       -> whereClause
                            -> A_Expr
                                    -> opname (if function has name else NULL)
                                    -> oper   (if operator is used else NULL)
                                    -> rexpr
                                            -> Attr
                                            OR
                                            -> A_Expr
                                            OR
                                            -> A_Const (value of constant)
                                    -> lexpr
```

## Transform Phase

* `SelectStmt -> Query (top level node)`
* Check if the `relname`(relation name) in the `fromClause` are know to the system.
* `RangeVar -> RTE`
* Check if the `attr`(attribute names) used are **present** in the `relations` given in the query.
* `ResTarget -> TLE`
* **Where**
* `A_Expr -> Expr`
* `Attr -> VAR` (similar to targetlist)
* The char strings representing the _relations_ and _attrs_ in the orginal tree are replaced by _relation ids_ and _VAR_ nodes whose fields are refferring to the entries of the _range table entry list_.

```Text
Query
From    :   -> rtable -> List(range table entry list)
                                                    -> RTE
                                                        -> relname
                                                        -> alias name
                                                        -> relation id

Select  :   -> targetList -> List
                                -> TLE
                                    -> resdom |     | -----> Resdom
                                                                -> resno
                                                                -> resname (name of the table)
                                    -> expr |   | ------> VAR
                                                            -> varno : (gives the position of the relation containing the current attribute in the range table entry list created above)
                                                            -> varattno : (gices the position of the attribute within the relation)

Where   :   -> qual
                -> Expr
                    -> opType
                    -> oper |   | -----> Oper
                                            -> opno
                                            -> opid
                    -> args : List
                                -> Expr
                                OR
                                -> VAR
                                    -> varno
                                    -> varattno
                                OR
                                -> Const
                                    -> constValue

```

## Generating Plan

```Text
MergeJoin
        -> lefttree (relation of join)
        -> righttree (relation of join)
        -> mergeclauses -> List
                            -> VAR
                                -> varno
```