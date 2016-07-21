```
cat /proc/interrupts | grep -e eth -e CPU
```
すると例えば↓下記のように表示される。
```
           CPU0       CPU1       
104:   15599497          0   PCI-MSI-edge      eth0
```
これはeth0の通信処理は全てCPU0で実行されていることを意味する
