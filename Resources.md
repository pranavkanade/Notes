# Resources

[TOC]

## Tutorials

### Python

#### Multi-Threading

1. [**Tutorial on Threads Programming with Python**](http://www.science.smith.edu/dftwiki/images/5/58/Matlof_PythonTutorial.pdf)
2. Debug

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

### Mac

1. [Shell](https://medium.com/@caulfieldOwen/youre-missing-out-on-a-better-mac-terminal-experience-d73647abf6d7)

### Linux

1. [ZSH](https://medium.com/wearetheledger/oh-my-zsh-made-for-cli-lovers-installation-guide-3131ca5491fb)

   a. install 

   ```bash
   apt install zsh
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
   ```

2. Font - [Fira Code](https://github.com/tonsky/FiraCode)

3. [Node.js](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-16-04)

   ```bash
   apt-get install curl python-software-properties
   curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
   apt-get install nodejs
   ```

4. vim -

   1. Config - 
      1. https://github.com/amix/vimrc
      2. https://vim-bootstrap.com/
   2. Tutorial
      1. https://vim-adventures.com/
      2. http://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/
      3. https://vimawesome.com/?q=cat%3Aother

5. tmux:

```bash
sudo apt-get update
sudo apt-get install tmux
```

​	1. tut : https://www.hamvocke.com/blog/a-guide-to-customizing-your-tmux-conf/

## Reference Posts

* [Exporting the git configuration](https://blog.praveen.science/best-way-to-import-or-export-the-git-configuration/)

