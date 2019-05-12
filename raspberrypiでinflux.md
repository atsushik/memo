```
curl -sL https://repos.influxdata.com/influxdb.key | sudo apt-key add -
#
sudo apt-get update
echo "deb https://repos.influxdata.com/debian stretch stable" | sudo tee /etc/apt/sources.list.d/influxdb.list
```

```
sudo apt-get update
sudo apt-get install telegraf
```
