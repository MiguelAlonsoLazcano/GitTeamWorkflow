# TerminalSetUp


# GIT 
Git Scripts for add GIT suppor to bash prompt profile 

* git-completion
* git prompt 


# VIMRC 
Vim config and common used plugins

* bash completition 
* file browser 

# TMUX 
Terminal multiplexer config file
	* sudo apt install tmux 
	* tmux depends on libevent and ncurses.



from: https://github.com/alonsodub/HostSetup

Miguel Angel (alonsodub.wordpress.com)
this are some files for Set up your Host machine 
and get a cool terminal. I still working in a Bash
script to do all this steps at once. This work for 
Ubuntu (Gnome) 


Set up 
===========================================
git clone https://github.com/alonsodub/HostSetup
cd HostSetup/

cp git-completion.bash ~/.git completion.bash                           
cp git-prompt.sh ~/.git-prompt.sh  
cat bash_profile_course >> ~/.bashrc

sudo apt-get install build-essential
sudo apt-get install vim git
sudo apt-get install bash-doc bash-completion

[OPCIONAL]
sudo apt-get install tmux
cp tmux.conf ~/.tmux.conf 

git config --global user.name "User Name"
git config --global user.mail "User Mail"
git config --global color.ui true
git config --global push.default upstream
git config --global merge.conflictstyle diff3

[OPCIONAL]
git config --global core.editor vim 

git clone https://github.com/aalonso/vimrc.git ~/.vim
cd ~/.vim
git submodule init 
git submodule sync 
git submoudle update 
ln -s ~/.vim/vimrc .vim 
