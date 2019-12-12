# wd

## 1. Install openjdk-8
```
sudo scp room107@10.0.2.220:/var/cache/apt/archives/* /var/cache/apt/archives/
```

```
sudo add-apt-repository ppa:openjdk-r/ppa -y
sudo apt-get update
sudo apt-get install openjdk-8-jdk git -y
sudo update-alternatives --config java
sudo update-alternatives --config javac
```

## 2. Install docker
```
sudo curl https://get.docker.com | bash
sudo rm /usr/local/bin/docker-compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## 3. Create user
```
sudo useradd -m wd
sudo usermod -aG docker wd
sudo passwd wd
```

## 4. install miniconda
```
sudo su wd
wget http://10.0.2.219/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
bash ~/miniconda.sh -b -p $HOME/miniconda
exit
```

## 5. install rapidminer studio
```
sudo su wd
wget http://10.0.2.219/rapidminer-studio-9.5.1.zip -O ~/rapidminer-studio-9.5.1.zip
cd ~
unzip rapidminer-studio-9.5.1.zip
exit
```
