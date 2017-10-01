# prerequesties
```
# sudo apt-get install -y alsa-utils sox libsox-fmt-all  alsa-oss libsdl2-dev libalsaplayer-dev
sudo apt-get install -y build-essential zlib1g-dev flex libasound2-dev libesd0-dev libsndfile1-dev
```
#
```
cd ~/git
#wget https://github.com/julius-speech/julius/archive/v4.4.2.tar.gz
#mv v4.4.2.tar.gz julius-v4.4.2.tar.gz
#tar zxvf julius-v4.4.2.tar.gz
#cd julius-4.4.2
git clone https://github.com/julius-speech/julius.git
cd julius
./configure --with-mictype=alsa --enable-words-int
# --enable-sp-segment ショートポーズセグメンテーションを行う
make
```

```
wget https://osdn.net/projects/julius/downloads/66544/dictation-kit-v4.4.zip
wget https://osdn.net/projects/julius/downloads/51159/grammar-kit-v4.1.tar.gz
unzip dictation-kit-v4.4.zip
tar zxvf grammar-kit-v4.1.tar.gz
```

- stand alone
```
cd ~/git/julius/dictation-kit-v4.4
~/git/julius/julius/julius -C main.jconf -C am-gmm.jconf -demo
```

- server-client
  - server
```
cd ~/git/julius/dictation-kit-v4.4
~/git/julius/julius/julius -C main.jconf -C am-gmm.jconf -demo -input adinnet
```
  - client
```
cd ~/git/julius
./adintool/adintool -in mic -out adinnet -server raspi3.local
```

## manual
- julius
  - https://julius.osdn.jp/refman/julius.html.ja
- adintool
  - https://julius.osdn.jp/juliusbook/ja/adintool.html

