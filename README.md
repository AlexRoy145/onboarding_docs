# Welcome to Devpipeline!

In this guide we will help you get started with the different tools that are needed to run our environments and develop our platforms.
If you have question/comments/concerns, Contact Alex Roy at 385-201-5645 (Text only please.)

## Package Manager

You need the Homebrew Package manager installed on the Macbook Pro, to install Homebrew:

1. Open your mac's terminal (command + space -> then type terminal into the spotlight search that appears and hit enter)
2. In your terminal paste --> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   After the installation is complete, you will need to close your terminal and reopen it.

## Xcode Command Line Tools

The Xcode command line tools are also required to use in our workflow process.

1. In your browser, visit https://developer.apple.com/download/more/ and sign in
2. Search --> command line tools.
3. Download the first "non beta entry ."

## Python

Python, pipenv and pip is needed for many of our backend projects, to install these packages:

1. In your newly oppened Terminal, paste --> (brew --prefix)/opt/python/libexec/bin
2. Once this is done, paste --> brew install pipx
3. Once completed, paste --> pipx ensurepath
4. Then paste --> pipx install pipenv

## Node

You need Javascript to develop on the frontend, to install:

1. Into your terminal, paste --> brew install node

## Git

We use Git for our development workflow, to install git:

1. In your terminal, paste --> git --version
2. If it is not installed, it will prompt you to install
3. in your terminal paste --> cd ~
4. Then paste --> vim .zshrc
5. In the open file, paste -->  
    setopt prompt*subst
   autoload -Uz vcs_info
   zstyle ':vcs_info:*' actionformats \
    '%F{5}(%f%s%F{5})%F{3}-%F{5}[%F{2}%b%F{3}|%F{1}%a%F{5}]%f '
   zstyle ':vcs*info:*' formats \
    '%F{5}(%f%s%F{5})%F{3}-%F{5}[%F{2}%b%F{5}]%f '
   zstyle ':vcs*info:(sv[nk]|bzr):*' branchformat '%b%F{1}:%F{3}%r'
   zstyle ':vcs*info:*' enable git cvs svn
   vcs*info_wrapper() {
   vcs_info
   if [ -n "$vcs_info_msg_0*" ]; then
   echo "%{$fg[grey]%}${vcs*info_msg_0*}%{$reset_color%}$del"fi}
   RPROMPT=$'$(vcs_info_wrapper)'
   export PATH="$PATH:/Users/alex/.local/bin"

6. After pasting this into the file, type :wq

## Postgress

Postgress is the database used by geotagging, to install:

1. Into your terminal paste --> brew install postgresql
2. Then paste --> brew services start posgres
3. In your terminal type --> createdb <your-profile-name>

## Visual Studio Code

Visual Studio Code is our code editing tool. It is Used to provide screenshare capabilities in the ide. To install:

1. visit https://code.visualstudio.com/download click the mac download.
2. Once Downloaded, open visual studio code, on the far right of the application, there is a symbol that looks like three boxes joined together,
   with one box seperated out, click on this symbol, a pannel should open up, in the search bar on the new pannel, search for --> liveshare
3. In the main window, click install.
4. Make sure you download VS Code into the Application folder for liveshare to work properly.
