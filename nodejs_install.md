- nodejsのインストール
```
# node.js、npmをapt-get 
sudo -E apt-get update
sudo -E apt-get install -y nodejs npm
# npmのキャッシュをクリーン
sudo -E npm cache clean
# node.jsバージョン管理「n」のインストール
sudo -E npm install npm n -g
# stable版のnode.jsにバージョンアップ
sudo -E n stable
# sudo -E n lts
```
