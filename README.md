# mac_dev_setup
Steps to setup my Mac.

## TODO

## Window Snapping
1. Is there a free and high quality window snapping utility that I can brew install?
    1. [Rectangle](https://rectangleapp.com/)
       1. [Rectangle brew](https://formulae.brew.sh/cask/rectangle)

## Install pyenv and the python version you would like to run

1. `brew install pyenv`
1. `echo 'PATH=$(pyenv root)/shims:$PATH' >> ~/.zshrc`
1. Confirm pyenv is in control and that only the system Python is available: `pyenv versions`
1. `pyenv install 3.10.2`
1. Set global default Python version to the latest: `pyenv global 3.10.2`
1. Confirm that the latest version of python is immediately set in the shell: `python -V`
