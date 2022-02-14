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
1. [Setup macOS 2021 For Optimal Command Line Productivity](https://matt.sh/setup-2021-late)
1. [How to use pyenv to run multiple versions of Python on a Mac](https://opensource.com/article/20/4/pyenv)

## TODO: REMOVE
1. [How to Automatically Setup Your MacBook for Development](https://towardsthecloud.com/automatically-setup-macbook-development)
1. [Mac Development Ansible Playbook](https://github.com/geerlingguy/mac-dev-playbook)
