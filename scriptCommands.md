
## Script 

The script used for this installation can be found in 

```bash
https://github.com/bitcoinsfacil/vps.git 
```

The script downloads, compiles and configures the masternodes from source. This will usually take between 5-15 minutes.


## Troubleshooting 



To watch available parameters: 

```bash
./install.sh
```


| Long Option  | Short Option | Values              | description                                                         |
| :----------- | :----------- | ------------------- | ------------------------------------------------------------------- |
| --project    | -p           | e.g. "myce"         | shortname for the project                                           |
| --net        | -n           | "4" / "6"           | ip type for masternode. (ipv)6 is default                           |
| --release    | -r           | e.g. "tags/v3.0.4"  | a specific git tag/branch, defaults to latest tested                |
| --count      | -c           | number              | amount of masternodes to be configured                              |
| --update     | -u           | --                  | update specified masternode daemon, combine with -p flag            |
| --sentinel   | -s           | --                  | for node monitoring                                                 |
| --wipe       | -w           | --                  | uninstall & wipe all related master node data, combine with -p flag |
| --help       | -h           | --                  | print help info                                                     |
| --startnodes | -x           | --                  | starts masternode(s) after installation                             |


To install 4 MYCE masternodes:

```bash
./install.sh -p myce -c 4
```

General configuration files per masternode installed 

```bash
ls /etc/masternodes/
```

After you finished installation do:

```bash
/usr/local/bin/activate_masternodes_myce
```     

To run a command on a MYCE masternode installed

```bash
/usr/local/bin/myce-cli -conf=/etc/masternodes/myce_n1.conf getinfo

```

To update a previously installed masternode:

```bash
./install.sh -p myce -u
```

