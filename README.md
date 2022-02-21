# mac_dev_setup
Steps to setup my Mac.

## TODO

## Mac background color change (to black) causes an issue
1. Consider commenting out for now

## What did not work in last install?
1. pyenv: consider following pyenv github repo instructions for installation rather than current script
1. repos script did not run. Did others not run? Consider manually triggering repos (all) script(s). Also, insert proper logs/info prompts.
1. Certain key programs are not installed: heroku cli, redis, miniconda. Consider brew installations or post-setup scripts.

## Consider: Do not auto-install pyenv and the python version you would like to run, e.g.:

1. `brew install pyenv`
1. `echo 'PATH=$(pyenv root)/shims:$PATH' >> ~/.zshrc`
1. Confirm pyenv is in control and that only the system Python is available: `pyenv versions`
1. `pyenv install 3.10.2`
1. Set global default Python version to the latest: `pyenv global 3.10.2`
1. Confirm that the latest version of python is immediately set in the shell: `python -V`
