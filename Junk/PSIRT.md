# PSIRT Plugin Development

* [Rational Team Concert extensions workshop](https://jazz.net/library/article/1000)
* Need jazz build engine (also called as `Build System Toolkit`)
* [Starting and stopping Jazz Build Engines](https://www.ibm.com/support/knowledgecenter/SSYMRC_6.0.2/com.ibm.team.build.doc/topics/tstartstopengine.html)
* [Eclipse Plugin Development](http://www.eclipse.org/pde/)
* [How to extend and customize Rational Team Concert for continuous integration](https://www.ibm.com/developerworks/library/d-extend-customize-rational-team-concert-continuous-integration/index.html)


* Connecting to Repository =>

```java
String repositoryURI = "http://";
ITeamRepository teamRepository = TeamPlatform.getTeamRepositoryService().getTeamRepository(repositoryURI);

```