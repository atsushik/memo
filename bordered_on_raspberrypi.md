```
#####
# install node-red
bash <(curl -sL https://raw.githubusercontent.com/node-red/raspbian-deb-package/master/resources/update-nodejs-and-nodered)
# let auto start the node-red
sudo systemctl enable nodered.service
