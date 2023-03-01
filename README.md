## Steps to set up a new Mac machine

1. Install Apple's Command Line Tools, which are prerequisites for Git and Homebrew.

```zsh
xcode-select --install
```
2. Clone repo into new hidden directory.

```zsh
# Use SSH ...
git clone git@github.com:IvanReyesO7/.dotfiles.git ~/.dotfiles
```

3. Create symlinks in the Home directory to the real files in the repository.

```zsh
ln -s ~/.dotfiles/.zshrc ~/.zshrc
ln -s ~/.dotfiles/.gitconfig ~/.gitconfig
```

4. Install Homebrew, and the software listed in the Brewfile.

```zsh

# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Then pass in the Brewfile location...
brew bundle --file ~/.dotfiles/Brewfile
```
