# Set Python Environment for Linux or Mac

## About

Easy way to switch between environments with simple bash scripts. 
Could be useful when working on multiple projects, microservices for example

## Linux

#### Download, unzip & install python 3.x.x

```bash
wget https://www.python.org/downloads/release/python-3xx/
tar -xvzf /path/to/yourfile.tgz /path/to/pythondir
./configure --prefix=/usr/local --enable-shared
export CC=clang
make
make install
```

#### Create venv

```bash
/path/to/installed/Python-3-x-x/bin/python3 -m venv ~/envs/my-env
```

#### CD into environments directory

```commandline
cd ~/envs
```

#### Create activation file

```commandline
vi activate_my_env.sh
```

#### Add to activate_my_env.sh:

```bash
cd ~/my-app
source ~/envs/my-env/bin/activate
```

#### Activate env:

```bash
chmod +x activate_my_env.sh
```

#### Create alias

```commandline
vi ~/.bashrc
```

#### Add to .bashrc:

```bash
alias my_env="source ~/envs/activate_my_env.sh"
```

#### CD into project directory & activate venv:

```commandline
my_env
```

## Mac OSx

#### Install python with Brew, specify version

```bash
brew install python@3.x
```

#### Create env

```bash
/usr/local/opt/python3.x/bin/python3 -m venv ~/envs/my-env
```

#### Create activate.sh

```commandline
cd ~/envs
vi activate_my_env.sh
```

#### Add to activate_my_env.sh:

```bash
cd ~/my-app
source ~/envs/my-env/bin/activate
```

#### Add alias

```commandline
vi ~/.zshrc
```

#### Add to .zshrc:

```bash
alias my_env="source ~/envs/activate_my_env.sh"
```

#### Activate alias

```commandline
source ~/.zshrc
```

#### CD into project directory & activate venv

```commandline
my_env
```

## Contacts

Mikhail Antonov *allelementaryfor@gmail.com*