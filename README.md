# mac_dev_setup
Steps to setup my Mac.

## First time setting up Mac

1. Language: English
1. Select Your Country or Region: United States
1. Accessibility
   1. Vision
      1. Appearance: Dark
1. Select Your Wi-Fi Network
1. Sign In With Your Apple ID
1. Account Name: vikram
1. Analytics: Do not share any information
1. Improve Siri & Dictation: Not Now
1. FileVault Disk Encryption: Turn on FileVault disk encryption
1. iCloud Keychain: Set up later
1. Apple Pay: Set up later

## Update software

1. Run Software Update, and ensure that the operating system is at the latest point release.

## iTerm2 Profile

1. Install iTerm2 Profile from dotfiles>zsh

## TODO

macos > setup.sh # Mac App Store
use pyenv to install latest version of python and make it global default
use dockutil to set the dock
retry packages, macos

## Install iTerm2

1. Install iTerm2: `brew install --cask iterm2`
   1. Install oh-my-zsh: `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
   1. Download and install powerline fonts (i.e. Fira Mono for Powerline): https://github.com/powerline/fonts
      1. ```
         # clone
         git clone https://github.com/powerline/fonts.git --depth=1
         # install
         cd fonts
         ./install.sh
         # clean-up a bit
         cd ..
         rm -rf fonts
      1. see: https://github.com/tomnomnom/dotfiles/blob/master/powerline-fonts.sh
   1. oh-my-zsh Theme (in zshrc): agnoster 
   1. iTerm configuration
      1. Colors > Color Presets...: `Tango Dark`
      1. Text > Font:
         1. `Fira Mono for Powerline`
         1. `Medium`
         1. `14`

## Install Homebrew

1. Install [Homebrew](https://brew.sh/): `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
1. Follow any next steps advised by Homebrew. For example, on Apple Silicon machines, Homebrew will provide commands to add Homebrew to your PATH.
1. Update and upgrade Homebrew: `brew update && brew upgrade`

## Install Ansible

1. `brew install python ansible`

## Install pyenv and the python version you would like to run

1. `brew install pyenv`
1. `echo 'PATH=$(pyenv root)/shims:$PATH' >> ~/.zshrc`
1. Confirm pyenv is in control and that only the system Python is available: `pyenv versions`
1. `pyenv install 3.10.2`
1. Set global default Python version to the latest: `pyenv global 3.10.2`
1. Confirm that the latest version of python is immediately set in the shell: `python -V`

## Set up Ansible playbook

1. Set up a directory structure for projects: code\[repository host]\[username]\[repository].
1. Git clone your fork of the [Mac Development Ansible Playbook](https://github.com/geerlingguy/mac-dev-playbook).
1. Create a `config.yml` in your local mac-dev-playbook that contains a list of packages and configuration settings that you want to apply to your environment.
1. Add your own dotfiles repository to `config.yml` to set up custom configurations for your software.

## References
1. [How to Set up an Apple Mac for Software Development](https://www.stuartellis.name/articles/mac-setup/)
1. [GitHub does dotfiles](https://dotfiles.github.io/)
1. [Dotfiles: automating macOS system configuration](https://kalis.me/dotfiles-automating-macos-system-configuration/)
  1. [rkalis/dotfiles](https://github.com/rkalis/dotfiles)
1. [Wes Bos' Command Line Power User Course](https://courses.wesbos.com/account/access/6208a5fd4407c61ab3ce1368)
1. [Oh My Zsh](https://ohmyz.sh/)
  1. [ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh)
1. [Setup macOS 2021 For Optimal Command Line Productivity](https://matt.sh/setup-2021-late)
1. [How to use pyenv to run multiple versions of Python on a Mac](https://opensource.com/article/20/4/pyenv)

## TODO
1. Install oh-my-zsh as part of bootstrap script: `$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
1. Install powerline fonts
1. Install zsh themes

## TODO: DELETE BELOW
1. [How to Automatically Setup Your MacBook for Development](https://towardsthecloud.com/automatically-setup-macbook-development)
1. [Mac Development Ansible Playbook](https://github.com/geerlingguy/mac-dev-playbook)
