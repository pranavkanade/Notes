# Resources

[TOC]

## Tutorials

### Python

#### Multi-Threading

1. [**Tutorial on Threads Programming with Python**](http://www.science.smith.edu/dftwiki/images/5/58/Matlof_PythonTutorial.pdf)

```python
import pdb
pdb.set_trace()  # this sets the break point
```



### Docker

0. Install 

   ```bash
   sudo apt-get update
   
   sudo apt-get install \
       apt-transport-https \
       ca-certificates \
       curl \
       software-properties-common
   
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   
   
   sudo apt-key fingerprint 0EBFCD88
   
   sudo add-apt-repository \
      "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
      $(lsb_release -cs) \
      stable"
   
   sudo apt-get update
   
   sudo apt-get install docker-ce
   
   sudo docker run hello-world
   
   ```

   

1. [Getting started with Docker in your project - a step by step tutorial](https://takacsmark.com/getting-started-with-docker-in-your-project-step-by-step-tutorial/)



### Git

1. [git-tutorial](https://backlog.com/git-tutorial/what-is-git/)



## Installation

### Linux

1. [ZSH](https://medium.com/wearetheledger/oh-my-zsh-made-for-cli-lovers-installation-guide-3131ca5491fb)

   a. install 

   ```bash
   apt install zsh
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
   ```

   