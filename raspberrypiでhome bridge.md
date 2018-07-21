```
sudo apt-get install npm libavahi-compat-libdnssd-dev git make
sudo npm install -g --unsafe-perm n
sudo n latest
sudo npm install -g --unsafe-perm homebridge

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
  "description": "This is an example configuration file. You can use this as a template for creating your own configuration file containing devices you actually own.",
  "accessories": [                                                            
  ],                                                                          
  "platforms": [         
  ]
}
EOF

```
