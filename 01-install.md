# MongoDB install
## On MacOS
### 1. Install Homebrew
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
> https://brew.sh/#install
### 2. Install MongoDB

    $ brew tap mongodb/brew
    $ brew install mongodb-community@4.4
    
### 3.Run MongoDB 

    $ brew services start mongodb-community@4.4
    $ brew services stop mongodb-community@4.4
    
   or
   
    $ mongod --config /usr/local/etc/mongod.conf --fork
    $ mongo
    
#### Exemple
    
    > show dbs
      admin   0.000GB
      config  0.000GB
      local   0.000GB


### 4. uninstall

    launchctl list | grep mongo
    launchctl unload ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist
    rm -f ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist
    launchctl remove homebrew.mxcl.mongodb
    pkill -f mongod
    rm -rf usr/local/etc/mongo.conf
    rm -rf <mongodb_folder>
    ls -al /usr/local/bin/mong*
    ls -al ~/Library/LaunchAgents
    rm -rf /usr/local/var/mongodb
    rm -rf /data/db
    
> https://medium.com/@rajanmaharjan/uninstall-mongodb-macos-completely-d2a6d6c163f9
### Create a service on MacOS
    
#### Exemple
    sudo launchctl start|stop postfix 
    
#### command
    sudo launchctl start mongod
    sudo launchctl stop mongod

#### Config Mongo
    cat usr/local/etc/mongo.conf
        systemLog:
          destination: file
          path: /usr/local/var/log/mongodb/mongo.log
          logAppend: true
        storage:
          dbPath: /usr/local/var/mongodb
        net:
          bindIp: 127.0.0.1

### Other Intsall
    > https://github.com/mongodb/homebrew-brew


### Other command
    ...
    
### You need to uninstall and install Homebrew
    
 As explained at https://github.com/Homebrew/install, I first ran 
        
        /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)" 
 
 After that I ran 
 
        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
