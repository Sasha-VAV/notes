```shell
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh -b -p $HOME/miniconda3
echo 'export PATH="$HOME/miniconda3/bin:$PATH"' >> ~/.bashrc
echo 'conda activate conda310' >> ~/.bashrc
source ~/.bashrc
```

```shell
pip install uv

```

```shell
poetry self update

poetry export -f requirements.txt --output requirements.txt
```

```shell
conda install jupyter notebook -y
```