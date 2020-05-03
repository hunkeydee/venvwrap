# venvwrap
A collection of bash functions for simple venv(python) mangement. 

## Install
[![demo] (https://asciinma.org/a/326321.svg)](https://asciinema.org/a/326321?autoplay=1)

## Usage
venvmk 
```~$ venvmk --help
  Create venv(s), installs pip, wheel, setuptools

  usage: venvmk <venv>...

  ex: `venvmk alpha` -> creates a venv called 'alpha'
  ex: `venvmk bravo charlie` -> creates two seperate venvs
```
venvrm 
```~$ venvrm --help
  Delete venv(s)

  usage: venvrm <venv>...

  ex: `venrm delta` -> deletes the venv called 'delta'
  ex: `venrm echo foxtrot` deletes two venvs
```
workon 
```~$ workon --help
  Enter/activate a venv

  usage: workon <venv>

  ex: `workon golf` -> activates the 'golf' venv context
```
venvex 
```~$ venvex --help
  Exit/deactivate the current venv

  usage: venvex

  ex: `venvex` -> deactivates the current venv
```
venvls 
```~$ venvls --help
  List all virtual environments managed by venvwrap

  usage: venvls
  
  ex `venvls` -> returns a dir listing of $VENV_HOME
```
venvpy 
```~$ venvpy --help
  Run python command in <venv>

  usage: venvpy <venv> <python cmd>

  ex: `venvpy hotel --version` -> returns python version for venv 'hotel'
```
venvpip 
```~$ venvpip --help
  Run a pip command in <venv>

  usage: venvpip <venv> <pip cmd>

  ex: `venvpip india show numpy` -> returns numpy details from venv 'india'
```
venvpkgls 
```~$ venvpkgls --help
  List packages installed or linked in <venv>(s)

  usage: venvpkgls <venv>...

  ex: `venpkgls juliet` -> runs pip list for 'juliet', then displays link in the site-packages directory
```
venvcmd 
```~$ venvcmd --help
  Run <cmd> in <venv>

  usage: venvcmd <venv> <cmd>
  
  ex: `venvcmd kilo python3 ./server.py` -> runs server.py in 'kilo' venv
```
venvinstall 
```~$ venvinstall --help
  Install pip package(s) in <venv>

  usage: venvinstall <venv> <pkg>...'

  ex: `venvinstall mike urllib3` -> installs urllib3 in 'mike'
  ex: `venvinstall november numpy chardet` -> installs numpy and chardet
```
venvlink 
```~$ venvlink --help
  link a package from <source_venv> to <target_venv>

  usage: venvlink <source_venv> <source_pkg> <target_venv>

  ex: venvlink oscar matplotlib papa` -> creates a link in 'papa' pointing to the matplotlib package in oscar
```

## Background
I didn't know enough about venvs or bash functions, so this was a weekend project inspired by virtualenvwrapper.  Instead of wrapping virtual-env, these functions support the built in python venv.

No effort was made to make this portable.  It works on Debian Buster.  Some dependencies include

- python3
- python3-venv
- python3-pip

- bash
- rm
- pushd/popd
- ln
- grep
- cut
