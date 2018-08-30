# Docker - Swarm

#### What is next step ?

Deploy your application onto a cluster, running it on multiple machines. *Multi-container, multi-machine applications are made possible by joining multiple machines into a **Dockerized** cluster call **SWARM***



#### Swarm Clusters 

> A swarm is a group of machines that are running Docker and joined into a cluster.

Once swarm cluster is ready, one can use docker commands as it is. The commands will now be executed on **Cluster** by a **Swarm Manager**. The machine can be physical or virtual. Each machine in a swarm is referred to as **nodes**.

The task distribution strategies can be specified by user in compose file.

> e.g. "Emptiest node", "Global"

**Swarm managers are the only machines in  a swarm that can execute commands.**  It also authorizes other machines to join the swarm as **worker**.

> Up until now, you have been using Docker in a single-host mode on your local machine. But Docker also can be switched into **swarm mode**, and that’s what enables the use of swarms. Enabling swarm mode instantly makes the current machine a swarm manager. From then on, Docker runs the commands you execute on the swarm you’re managing, rather than just on the current machine. 



#### Setting up your swarm

