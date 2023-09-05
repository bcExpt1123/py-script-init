## Install pyenv
```
sudo apt update -y

curl --version

# If you don't have, install the curl using:
sudo apt-get install curl

curl https://pyenv.run | bash
```

## Pre Run for pyenv
```
source ./.bashrc

pyenv install --list | grep "3.[6789]"

pyenv install -v 3.9

python --version

pyenv global 3.9.18

pyenv versions
```

```
python --version
# Python 3.9.18
```

```
python -m pip install jupyterlab

python -m pip install notebook

python -m jupyter notebook
```

## Run
```
python -m jupyter notebook
```

# TroubleShoot

```
RuntimeError: Your system has an unsupported version of sqlite3. Chroma requires sqlite3 >= 3.35.0.

# Run following command
python -m pip install pysqlite3-binary

# Add these lines to the top of your app

__import__('pysqlite3')
import sys
sys.modules['sqlite3'] = sys.modules.pop('pysqlite3')
```

## Virtual ENV
```
python -m pip install virtualenv
python -m virtualenv venv
source venv/bin/activate

```