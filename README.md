# API Mockuper

A aplication that serve the logic to manage the design of a software development


## Requirements
* node js 6
* sails js 0.12.4
* MongoDB version: 2.6.5

## Installation

* 1.  npm install
* 2.  mkdir data
* 3.  mongod --dbpath=data
* 4.  mongo
      db.createUser({
        user: "accountUser",
        pwd: "password",
        roles: [ 
          "readWrite", 
          "dbAdmin" 
        ]
      })
* 5. mongo
db.permission.insert( { can: "edit" } )
      db.permission.insert( { can: "view" } )
      
## Run unit test
mocha test/bootstrap.test.js test/integration/**/*.test.js


## Run
* sails lift
* http://localhost:1337/

## Docker installation

* docker build -t llll/api .
* docker run -p 1337:1337 -d llll/api
* docker logs containerId
* docker stop  containerId
* curl -i localhost:1337


