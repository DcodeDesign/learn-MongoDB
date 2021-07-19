# Save Database
    cd ~/Desktop/backupdb
    mongodump
    mongodump --help
    mongodump -d test
    mongodump -d test -o testBckp
    mongorestore dump
    
    mongoexport -d test -c users -o users.json
    mongoexport --help
    mongoimport -d test users.json
    mongoimport --help
    
    mongoexport -d test -c users --fields=name --type=csv -o users.csv
    

