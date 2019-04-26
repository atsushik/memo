# basics
```
sudo apt update && sudo apt -y upgrade && sudo apt -y autoremove
sudo apt -y install screen htop git cmake
```

# jetson-inference https://github.com/dusty-nv/jetson-inference/blob/master/docs/building-repo-2.md
```

mkdir -p ~/git
cd ~/git
git clone https://github.com/dusty-nv/jetson-inference
cd jetson-inference
git submodule update --init
mkdir build
cd build
cmake ../
```


# python
```
sudo apt install python3-pip
pip3 install h5py
#sudo apt install python3-scipy python3-keras
pip3 install scipy
pip3 install numpy
pip3 install keras
pip3 install pillow
pip3 install pandas
sudo pip3 install scikit-learn
pip3 install matplotlib
sudo pip3 install Jetson.GPIO
```

# tensorflow
```
sudo apt-get install libhdf5-serial-dev hdf5-tools
pip3 install --extra-index-url https://developer.download.nvidia.com/compute/redist/jp/v42 tensorflow-gpu==1.13.1+nv19.3 --user
```

# pyTorch
```
wget https://nvidia.box.com/shared/static/veo87trfaawj5pfwuqvhl6mzc5b55fbj.whl -O torch-1.1.0a0+b457266-cp36-cp36m-linux_aarch64.whl
pip3 install numpy torch-1.1.0a0+b457266-cp36-cp36m-linux_aarch64.whl
git clone https://github.com/pytorch/vision
cd vision
sudo python setup.py install
```

# opencv
```
#swap領域(ここでは6GB)の作成
fallocate -l 6G swapfile
chmod 600 swapfile
mkswap swapfile
sudo swapon swapfile
#swap領域が設定されているかの確認
free -m

cd
wget https://raw.githubusercontent.com/AastaNV/JEP/master/script/install_opencv4.0.0_Nano.sh
chmod 774 install_opencv4.0.0_Nano.sh
./install_opencv4.0.0_Nano.sh ~
```

