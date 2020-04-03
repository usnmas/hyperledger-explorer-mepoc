# Hyperledger Explorer

Hyperledger Explorer Use Case 


## Prerequisites

- Nodejs 10 and 12 (10.19 and 12.16 tested)
- PostgreSQL 9.5 or greater
- jq
- git clone https://github.com/hyperledger/blockchain-explorer.git


## Installation Guide 

**`jq install`**

$ sudo apt-get update -y

$ sudo apt-get install -y jq




**`Git Clone`**

~$ git clone https://github.com/hyperledger/blockchain-explorer.git




**`PostgreSQL Install`**

~$ sudo apt-get update

~$ sudo apt-get install postgresql postgresql-contrib

~/blockchain-explorer/app/persistence/fabric/postgreSQL$ chmod -R 775 db

~/blockchain-explorer/app/persistence/fabric/postgreSQL/db$ sudo -u postgres ./createdb.sh


`Update PostgreSQL database setting (optional)`

~/blockchain-explorer/app/explorerconfig.json file modification 


`Database Creation Check`

~/blockchain-explorer/app/persistence/fabric/postgreSQL/db$ sudo -u postgres psql

\l to list up database

Ctrl+Z to exit 


`Configure Hyperledger Fabric (Modify connection profile)`

Certificate Path & grpc (rather than grpcs)

~/blockchain-explorer/app/platform/fabric/connection-profile/first-network.json


`Build Hyperledger Explorer`

~/blockchain-explorer$ npm install

~/blockchain-explorer$ cd app/test

~/blockchain-explorer/app/test$ npm install

~/blockchain-explorer/app/test$ npm run test

~/blockchain-explorer/app/test$ cd ../../client

~/blockchain-explorer/client$ npm install

~/blockchain-explorer/client$ npm run test:ci -- -u --coverage (Error : OK) 

~/blockchain-explorer/client$ npm run build


`Run & Stop Hyperledger Explorer`

~/blockchain-explorer$ ./start.sh

~/blockchain-explorer$ ./stop.sh


`Access Hyperledger Explorer`

http://host:8080


## Reference 

- Reference (Install Guide & Sources) : [Hyperledger Explorer](https://github.com/hyperledger/blockchain-explorer)
- Git Repository (Clone) : [Hyperledger Git Repository](https://github.com/hyperledger/blockchain-explorer.git)
