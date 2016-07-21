+ INSTALL
  ```
  # Data Collector
  wget https://dl.influxdata.com/telegraf/releases/telegraf-0.13.1.x86_64.rpm
  sudo yum localinstall -y telegraf-0.13.1.x86_64.rpm
  # Time-Series Database
  wget https://dl.influxdata.com/influxdb/releases/influxdb-0.13.0.x86_64.rpm
  sudo yum localinstall -y influxdb-0.13.0.x86_64.rpm
  # Data Visualization & Graphing
  wget https://dl.influxdata.com/chronograf/releases/chronograf-0.13.0-1.x86_64.rpm
  sudo yum localinstall -y chronograf-0.13.0-1.x86_64.rpm
  # Alerting & Data Processing
  wget https://dl.influxdata.com/kapacitor/releases/kapacitor-0.13.1.x86_64.rpm
  sudo yum localinstall -y kapacitor-0.13.1.x86_64.rpm
  ```
+ SETUP
  ```
  sudo service telegraf restart
  # 設定ファイルは /etc/influxdb/influxdb.conf
  # http://localhost:8086
  sudo /etc/init.d/influxdb restart
  # ↓ 127.0.0.1 を 0.0.0.0 に変更
  # sudo vim /opt/chronograf/config.toml
  # http://127.0.0.1:10000
  sudo service chronograf restart
  ```
+ RUN
+ DAILY
