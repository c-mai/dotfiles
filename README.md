# dotfiles
this is a bare repo that is used to manage dotfiles

## Steps to install on fresh linux system

Start in the home directory

Make sure the repo doesn't track itself might get infinite recursion:
```
echo ".dotfiles" >> .gitignore
```

Clone this repo:
```
git clone https://github.com/c-mai/dotfiles.git $HOME/.dotfiles
```

Set up alias for this bare git repo:
```
alias dotfiles='usr/bin/git --git-dir=$HOME/.dotfiles --work-tree=$HOME'
```

Don't show Untracked Files:
```
dotfiles config --local status.showUntrackedFiles no
```

Checkout the repo to the home directory
```
dotfiles checkout
```
If there is an error msg back up and delete the files that would be overwritted by checkout

## Usage for updating this repo
