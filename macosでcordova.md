- nodebrewをinstall
```
curl -L git.io/nodebrew | perl - setup
echo 'export PATH=$HOME/.nodebrew/current/bin:$PATH' >> ~/.bashrc
. ~/.bashrc 
```

- nodeをinstall
```
nodebrew help
nodebrew install-binary stable
nodebrew ls
nodebrew use stable
```

- cordovaをinstall
```
npm install -g cordova
cordova -v
```

- cordovaの動作確認のためにプロジェクトを作成して試す
```
cordova create MyApp
cd MyApp/
cordova platform add browser
cordova run browser
```

- xcodeをapp storeからinstall

- xcodeのコマンドラインツールをinstall
```
xcode-select --install
sudo xcodebuild -license
# agree する
```

- さっきの動作確認用のプロジェクトにiOSプラットフォームを追加して実行
```
cd MyApp/
cordova platform add ios
cordova run ios
```
