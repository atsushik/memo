# prerequesties
```
sudo apt-get install alsa-utils sox libsox-fmt-all
```
#
```
wget https://github.com/julius-speech/julius/archive/v4.4.2.tar.gz
mv v4.4.2.tar.gz julius-v4.4.2.tar.gz
tar zxvf julius-v4.4.2.tar.gz
cd julius-4.4.2
./configure
make
```

```
wget https://osdn.net/projects/julius/downloads/66544/dictation-kit-v4.4.zip
wget https://osdn.net/projects/julius/downloads/51159/grammar-kit-v4.1.tar.gz
unzip dictation-kit-v4.4.zip
tar zxvf grammar-kit-v4.1.tar.gz
```

```
cd /home/pi/git/julius-4.4.2/dictation-kit-v4.4
/home/pi/git/julius-4.4.2/julius/julius -C main.jconf -C am-gmm.jconf -demo
```
