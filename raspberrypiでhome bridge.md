```
#
sudo apt-get install npm libavahi-compat-libdnssd-dev git make
sudo npm install -g --unsafe-perm n
sudo n latest
sudo npm install -g --unsafe-perm homebridge

#
sudo npm install -g pm2
pm2 startup
# Follow the instructions on screen. #######################

#
cd ~/.homebridge
pm2 start homebridge
pm2 save

#
sudo npm install -g --unsafe-perm homebridge-config-ui-x

#
npm install -g homebridge-people

```

```
mkdir -p ~/.homebridge
touch ~/.homebridge/config.json
cat <<EOF > ~/.homebridge/config.json
{
    "bridge": {
        "name": "Homebridge",
        "username": "DE:AD:BE:EF:00:00",
        "port": 51826,
        "pin": "031-45-154"
    },                                                                          
    "accessories": [
    ],
    "platforms": [
        {
            "description": "homebridge-people",
            "platform": "People",
            "threshold" : 15,
            "anyoneSensor" : true,
            "nooneSensor" : false,
            "webhookPort": 51828,
            "cacheDirectory": "./.node-persist/storage",
            "pingInterval": 10000,
            "ignoreReEnterExitSeconds": 0,
            "people" : [
                {          
                    "description": "homebridge-people",
                    "name" : "MY_NAME",
                    "target" : "my_phone.local",                  
                    "threshold" : 15,
                    "pingInterval": 10000,
                    "ignoreReEnterExitSeconds": 0
                }
            ]
        },
        {
            "description": "homebridge-config-ui-x",
            "platform": "config",
            "name": "Config",
            "port": 8080,
            "sudo": false
        }
    ]
}
EOF
# DONT FORGET TO FIX MAC ADDRESS IN config.json
```
