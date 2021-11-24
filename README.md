# .dotfiles

1. Install Apple's Command Line Tools, which are prerequisites for Git and Homebrew.

```sh
xcode-select --install
```

2. Clone repo into new hidden directory

```sh
#Use SSH (if set up)
git clone git@github.com:seanbrwh/.dotfiles.git ~/.dotfiles
```

3. Create symlinks in the Home directory to the real files in the repo

```sh
# There are better and less manual ways to do this
# Investigate install scripts and bootstrapping tools

ln ~/.dotfiles/[.dotfile] ~/[.dotfile]
```

4. Install Homebrew, followed by the software listed in the Brewfile

```sh
# These could also be included in an install script
# Install Homebrew
/bin/bash -c "$(curl -fsSL
https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Then pass in the Brewfile location...
brew bundle --file ~/.dotfiles/Brewfile

cd ~/.dotfiles && brew bundle

```

TODO List

- Learn how to use defaults to record and restore system prefrences and other macOS configurations

- Organize these growing steps into multiple script files

- automate symlinking and run script with a bootstraping tool like dotbot

- revisit the list in zshrc to customize the shell

- make a checklist of steps to decommission your computer before wiping your hard drive

- create a bootable usb installer for mac os

- integrate other cloud services into your dotfile process (dropbox, google drive, etc)

- find inspiration and examples of other dotfiles at dotfiles.github.io
