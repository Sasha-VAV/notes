Launch vm
```shell
docker run --gpus all -itd -v ~/vm/home:/home --name vm --network ask4game -p 127.0.0.1:2222:22 nvidia/cuda:12.2.2-base-ubuntu22.04
docker exec -it vm bash
adduser alex
```

New user and basic dependencies
```shell
apt update
apt install -y sudo vim iproute2
usermod -aG sudo alex
su alex
```

To home dir
```shell
sudo whoami
cd
```

ssh on docker
```shell
sudo apt install openssh-server -y
sudo mkdir -p /var/run/sshd
sudo ssh-keygen -A
sudo service ssh start
```

conda
```shell
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh -b -p $HOME/miniconda3
echo 'export PATH="$HOME/miniconda3/bin:$PATH"' >> ~/.bashrc
echo 'conda activate conda310' >> ~/.bashrc
source ~/.bashrc
```