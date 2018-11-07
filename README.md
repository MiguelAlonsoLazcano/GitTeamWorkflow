# TerminalSetUp

Miguel Angel (alonsodub.wordpress.com)
This are some files for Set up your Host machine and get a cool terminal. I still working in a Bash script to do all this steps at once. This work for Ubuntu (Gnome)

## GIT
Git support scripts for git prompt and git completion

* git-completion.bash
* git-prompt.sh
* bash_profile

## VIMRC
Vim config and common used plugins

* bash completition 
* file browser 

## TMUX
Terminal multiplexer configuration file 
    * tmux depends on libevent and ncurses.


## Set up
===========================================
### Install basic packages
```bash
sudo apt install build-essential
sudo apt install vim git
sudo apt install bash-doc bash-completion
```

### Git scripts
```bash
git clone https://github.com/MiguelAlonsoLazcano/TerminalSetUp
cd TerminalSetup/
```

```bash
cp git/git-completion.bash ~/.git completion.bash
cp git/git-prompt.sh ~/.git-prompt.sh
cat git/bash_profile_course >> ~/.bashrc
```

### Git configuration
```bash
git config --global user.name "User Name"
git config --global user.mail "User Mail"
git config --global color.ui true
git config --global push.default upstream
git config --global merge.conflictstyle diff3
```

## Terminal multiplexor
```bash
sudo apt install libevent ncurses
sudo apt install tmux
cp tmux/tmux.conf ~/.tmux.conf
```

## Vim
```bash
git config --global core.editor vim 

git clone https://github.com/aalonso/vimrc.git ~/.vim
cd ~/.vim
git submodule init 
git submodule sync 
git submodule update
ln -s ~/.vim/vimrc .vim 
```
