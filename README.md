# wd
## Usage
### 1. Login as wd user
### 2. Open Terminal
### 3. Active miniconda
```
source ~/miniconda/bin/active
```
### 4. Open Rapidminer Studio
```
cd ~/rapidminer-studio
./RapidMiner-Studio.sh
```

## Installation
### 1. Install openjdk-8
```
sudo add-apt-repository ppa:openjdk-r/ppa -y
sudo apt-get update
sudo apt-get install openjdk-8-jdk git -y
sudo update-alternatives --config java
sudo update-alternatives --config javac
```

### 2. Install docker
```
sudo curl https://get.docker.com | bash
sudo rm /usr/local/bin/docker-compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

### 3. Create user
```
sudo useradd -m wd
sudo usermod -aG docker wd
sudo passwd wd
```

### 4. Install miniconda
```
sudo su wd
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
bash ~/miniconda.sh -b -p $HOME/miniconda
exit
```

### 5. Install rapidminer studio
```
sudo su wd
wget https://releases.rapidminer.com/latest/rapidminer-studio/rapidminer-studio.zip -O ~/rapidminer-studio-9.5.1.zip
cd ~
unzip rapidminer-studio-9.5.1.zip
exit
```
