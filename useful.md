# Useful Commands

[TOC]

## CTAGS

Keyboard command | Action |
---|--|
Ctrl-] | Jump to the tag underneath the cursor|
:ts <tag> <RET> | Search for a particular tag |
:tn | Go to the next definition for the last tag |
:tp | Go to the previous definition for the last tag|
:ts | List all of the definitions of the last tag|
Ctrl-t | Jump back up in the tag stack|

## Commands In Need

### To mount the `/nfs` dir on your system

```mount nzbign-a:/vol/vol_releng_packages  /nfs/builds```

## REGEX to eliminate date and rubbish stuff from pg.log

(2018-05-08 01:[0-9]*:[0-9]*.[0-9]* EDT \[[0-9]*\]  DEBUG:  )

## LSCM

### Retarget

lscm workspace change-target -r https://jazzsdi04.svl.ibm.com:9445/ccm/ prak_7216p3 nps.dev-Staging-7.2.1.6-P3

### Base line creation for upgrade component

lscm create baseline -r https://jazzsdi04.svl.ibm.com:9445/ccm  upgrade_120709 RTC_121533_2018_05_08 upgrade

lscm deliver -b 1901

### Login

lscm login -c -r https://jazzsdi04.svl.ibm.com:9445/ccm -u prakanad@in.ibm.com

### Create 

lscm create workspace -r https://jazzsdi04.svl.ibm.com:9445/ccm -s nps.rel-7.2.1.3-P3 7213p3

### Load

lscm load -r https://jazzsdi04.svl.ibm.com:9445/ccm --all supp_tools_Workspace

### Checkin

lscm checkin -c 1930 /nzscratch/7216p1/sst/mfraase_bin/nz_csn_log_capture

### Comment

lscm changeset comment 1946 "Utility to capture the logs related to particular csn"

## Database Commands

### Stored Procedures

#### Creating

CREATE OR REPLACE PROCEDURE ADMIN.tryout(INTEGER, INTEGER) RETURNS BOOLEAN language nzplsql  EXECUTE AS OWNER  AS BEGIN_PROC BEGIN
update t set a=1 where b=2;
...
RETURN TRUE; END; END_PROC;

#### Drop

drop procedure TRYOUT(INTEGER, INTEGER);

#### How many stored procedures

SELECT OBJID, PROCEDURE from _V_PROCEDURE;

#### Source code

SELECT PROCEDURESOURCE from "SYSTEM.ADMIN._V_PROCEDURE" WHERE OBJID=1761713;

## Nzstart not working

* look at `/nz/.upgrade.state` or `/nz/var/lib/nzdontstart`

## Trex

* The location -> `/nzscratch/nzt.rel-7.2.0.9-P2_vm-dw37/nps.global/nps.global.tools/trex`
* Command to execute -> `setsid sh run_trex.sh input.txt > trex.out 2>&1 &`
* output file -> `trex.out`