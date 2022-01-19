# dotfiles

## Instructions for Custom dev workspace 

#Changing Shell from Bash to ZSH 

sudo apt install zsh 

chsh -s $(which zsh)

logout 

#test that it worked 
echo $SHELL 

#Install oh-my-zsh 

sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

#change the theme in the .zshrc to agnoster 

nano .zshrc 

source .zshrc 

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

#change the theme in the .zshrc to powerlevel10k/powerlevel10k 

#Add ZSH Plugins 

git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

#back into the .zshrc make the plugins add with 

nano .zshrc

zsh-autosuggestions zsh-syntax-highlighting

#Gnome Extensions 

sudo apt install chrome-gnome-shell
sudo apt install gnome-tweaks

#Visit https://extensions.gnome.org/ in your web browser 

#Install the following: 
#    - Caffeine 
#    - CPU Power Manager
#    - Dash to Dock 
#    - Desktop Icons 
#    - User Themes 

#Now we can really start to customise with the following 

#https://draculatheme.com/

#Gnome Terminal 
git clone https://github.com/dracula/gnome-terminal
cd gnome-terminal
./install.sh
cd 

#From terminal or automated  
#Theme 
cd Downloads 
wget https://github.com/dracula/gtk/archive/master.zip
sudo unzip master.zip -d /usr/share/themes && sudo mv /usr/share/themes/gtk-master /usr/share/themes/Dracula
gsettings set org.gnome.desktop.interface gtk-theme "Dracula"
gsettings set org.gnome.desktop.wm.preferences theme "Dracula"

#Icons
wget https://github.com/dracula/gtk/files/5214870/Dracula.zip
sudo unzip Dracula.zip -d /usr/share/icons
gsettings set org.gnome.desktop.interface icon-theme "Dracula"

#Logout and back in

#Background change

#Download my dotfiles from github 

git clone https://github.com/MichaelCade/dotfiles.git

#change desktop background to CachedImage_3840_1080_POS4.jpg
