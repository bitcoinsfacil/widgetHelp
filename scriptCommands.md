
## Script 

The script used for this installation can be found in 

```
https://github.com/bitcoinsfacil/vps.git 
```

The script downloads, compiles and configures the masternodes from source. This will usually take between 5-15 minutes.


## Troubleshooting 



To watch available parameters: 

```./install.sh```


To install 4 MYCE masternodes:
```
./install.sh -p myce -c 4
```

General configuration files per masternode installed 

```ls /etc/masternodes/```

After you finished installation do:

```
/usr/local/bin/activate_masternodes_myce
```     

To run a command on a MYCE masternode installed

```
/usr/local/bin/myce-cli -conf=/etc/masternodes/myce_n1.conf getinfo

```

