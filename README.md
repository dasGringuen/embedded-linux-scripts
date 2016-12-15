# Embedded Linux and remote host connection scripts
Set of scripts to make easier the connection and browsing file systems of remote hosts through ssh.
Written in Python 3

Adrian Remonda 2016

## Requirements

* python3
* ssh

## Install

```sh
    ~$ ./install.py
```

## Setup and customize
1. Create a generic initialization file. This will create a configuration file called _el.conf_ in the current directory. This file will determine the ip address of the host and some other options.

```sh
    ~$ elinit
```
    
2. Customize the el.conf file created in the previous step
```sh
    user="ad"               # remote login user name
    ip="localhost"          # remote host address or domain name
    file_manager="nautilus" # File manager can specify Nautilus, Dolphin or any other
```

3.  To avoid writing the remote password everytime (Optional)
    The public key will be copied to the remote host
    
    ~$ elsetup_remote_host
    
## Use
### Ping the remote host

    ~$ elping

### Connect using ssh

    ~$ elconn
    
### To browse remote file system 
It will run the file manager configured in step 2

    ~$ elfs
    
### Todos

 - Have one script, instead of having them separated. Should include autocomplete with TAB
 
### License

-   GPL v2

**Free Software**

