# StudyFinder Project

## Description

StudyFinder matches students from UWA who are studying similar units and are available at similar times so they can meetup and study together.

The StudyFinder project was designed with the purpose to develop a matching application similar to Tinder, Plenty of Fish, OkCupid etc.

It can be viewed here: https://study-finder.herokuapp.com/

**Note:** The site may take a few seconds to load upon the initial visit as Heroku servers are designed to sleep after a short period of time. This means if no one has accessed the site for a while the server will take a bit of time to wake-up and respond to the request.

If you don't want to go through the account creation process and would rather just jump straight in and see how the application works feel free to use this account:

**Login:** 01010101@student.uwa.edu.au

**Password:** password

## Installation

### Install Express
```
npm install -g express-generator
```

### Install nodemon
```
npm install -g nodemon
```

### Install dependencies
CD To the CITS3403 directory and run:
```
npm install
```

### Install mongoDB & Using MongoDB
**REMOTE**

Application is already setup to run with a remote database.

Remote DB URI: 'mongodb://erklik:tusif556571@ds147681.mlab.com:47681/cits3403mac'

**LOCAL**

Open db.js in the 'routes' directory.

Comment out the remote DB URI.
Uncomment the local DB URI.

After adding mongod to PATH, create a data directory.

```
md \data
```
```
md \data\db
```
Start mongod
```
mongod
```
### Import unit data to the DB
Copy the CSV file to MongoDB /bin/ and run:
```
mongoimport -d CITS3403 -c units --type csv --file units.csv --headerline
```
### Start the server
```
nodemon npm start
```
or
```
npm start
```
Currently opens on port 3000.

Access locally here: http://127.0.0.1:3000/

## Authors

Jim Reynolds

Jason Ankers

Maktoom Ahmed

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE.md](LICENSE.md) file for details.
