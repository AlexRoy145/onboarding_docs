Welcome to Devpipeline!
=======================

In this guide we will help you get started with the different tools that are needed to run our environments and develop our platforms.
  
Package Manager
---------------
For the rest of this guide we will need Homebrew Package manager, to install Homebrew:
1. Open your mac's terminal (command + space -> then type terminal into the spotlight search that appears and hit enter)
2. Into your terminal paste --> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
After the installation is complete, you will need to close your terminal and reopen it.   

Xcode Command Line Tools
------------------------
The xcode command line tools are required for several of the below downloads  
1. In your browser, visit https://developer.apple.com/download/more/ and sign in
2. search --> command line tools
3. download the first non beta entry  

Python
------
Pthon, pipenv and pip will be needed for many of our backend projects, to install these:
1. In your newly oppened Terminal, paste --> (brew --prefix)/opt/python/libexec/bin
2. Once this is done, paste --> brew install pipx
3. Once completed, paste --> pipx ensurepath
4. Then paste --> pipx install pipenv  

Node
----
Javacript will be needed to develop on the frontend, to install:
1. Into your terminal, paste --> brew install node  


Git
---
Git is bassically a requirement to develop, to install git:
1. In your terminal, paste --> git --version
2. If it is not installed, it will prompt you to install
3. in your terminal paste --> cd ~
4. then paste --> vim .zshrc
5. in the open file, paste -->  
setopt prompt_subst
autoload -Uz vcs_info
zstyle ':vcs_info:*' actionformats \
    '%F{5}(%f%s%F{5})%F{3}-%F{5}[%F{2}%b%F{3}|%F{1}%a%F{5}]%f '
zstyle ':vcs_info:*' formats       \
    '%F{5}(%f%s%F{5})%F{3}-%F{5}[%F{2}%b%F{5}]%f '
zstyle ':vcs_info:(sv[nk]|bzr):*' branchformat '%b%F{1}:%F{3}%r'

zstyle ':vcs_info:*' enable git cvs svn

# or use pre_cmd, see man zshcontrib
vcs_info_wrapper() {
  vcs_info
  if [ -n "$vcs_info_msg_0_" ]; then
    echo "%{$fg[grey]%}${vcs_info_msg_0_}%{$reset_color%}$del"
  fi
}
RPROMPT=$'$(vcs_info_wrapper)'

# Created by `userpath` on 2021-02-01 18:26:02
export PATH="$PATH:/Users/alex/.local/bin"  

Postgress
---------
Postgress is the database used by geotagging, to install:
1. Into your terminal paste --> brew install postgresql
2. Then paste --> brew services start posgres


