# mac_dev_setup
Steps to setup my Mac.

## TODO

## Oh My Zsh
1. Can I check if this is already installed?
    1. https://www.codegrepper.com/code-examples/shell/how+to+check+if+oh+my+zsh+is+installed

## Powerline fonts
1. Can I check if this is already installed?

## Install pyenv and the python version you would like to run

1. `brew install pyenv`
1. `echo 'PATH=$(pyenv root)/shims:$PATH' >> ~/.zshrc`
1. Confirm pyenv is in control and that only the system Python is available: `pyenv versions`
1. `pyenv install 3.10.2`
1. Set global default Python version to the latest: `pyenv global 3.10.2`
1. Confirm that the latest version of python is immediately set in the shell: `python -V`
