# zsh-config
Contains the configuration of my zsh-file

Here is the quick setup guide:
```bash
# Intall zsh
sudo apt install zsh

# Setting up oh my zsh
# ref : https://github.com/ohmyzsh/ohmyzsh?tab=readme-ov-file#basic-installation
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# auto suggestion 
# ref : 
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# syntax highlighting
# ref :https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md#oh-my-zsh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# Now add this to your ~/.zshrc file
# plugins=( [plugins...] zsh-autosuggestions zsh-syntax-highlighting themes)
source ~/.zshrc

# Set zsh as default shell
# ref : https://stackoverflow.com/questions/246128/how-to-change-default-shell-in-linux
chsh -s $(which zsh)

# TO set bash as default shell again
chsh -s $(which bash)

# install fzf 
# ref : https://github.com/junegunn/fzf?tab=readme-ov-file#using-git
# using this because we get the latest version
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install

# Add the nvm configs to the .zshrc file
# generally they are
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

# To set the powerlevel10k theme
# ref :https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"

# Now set the theme in the .zshrc file
# ZSH_THEME="powerlevel10k/powerlevel10k"
```