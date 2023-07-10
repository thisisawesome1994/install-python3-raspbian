# install-python3-raspbian

apt-get update
apt upgrade -y
apt-get install -y build-essential tk-dev libncurses5-dev libncursesw5-dev libreadline6-dev libdb5.3-dev libgdbm-dev libsqlite3-dev libssl-dev libbz2-dev libexpat1-dev liblzma-dev zlib1g-dev libffi-dev
wget https://www.python.org/ftp/python/3.8.0/Python-3.8.0.tgz    
tar zxf Python-3.8.0.tgz
cd Python-3.8.0
./configure --enable-optimizations
make -j 4
make altinstall
echo "alias python=/usr/local/bin/python3.8" >> ~/.bashrc
source ~/.bashrc
