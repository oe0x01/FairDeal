# Fair Deal

<p>
  <img src="https://img.shields.io/badge/React-16.8.+-lightblue.svg">
  <img src="https://img.shields.io/badge/Semantic UI-0.88.+-purple.svg">
  <img src="https://img.shields.io/badge/Nodejs-8.10.+-green.svg">
  <img src="https://img.shields.io/badge/Express-4.16.+-black.svg">
  <img src="https://img.shields.io/badge/MySQL-5.7.+-blue.svg">
</p>

FairDeal is an open source e-Commerce application which emphasises on swapping / exchanging. 
It is written in Express.js and React.js with Semantic UI.

## Installation

Step 1, clone this repo

Step 2, add the **_.env_** file in **server** directory with environment settings:

```
tokenSecret=REPLACE_THIS_WITH_ANY_LONG_RANDOM_STRING
dbHost=MYSQL_SERVER_CONNECTION_STRING
dbUser=MYSQL_USER
dbPassword=MYSQL_USER_PASSWORD
dbName=MYSQL_DATABASE_NAME
testDbName=MYSQL_DATABASE_NAME_FOR_INTEGRATION_TEST
sendgridApiKey=SENDGRID_API_KEY
sendgridDailyLimit=SENDGRID_DAILY_LIMIT_FOR_FREETIER
elasticemailApiKey=ELASTICEMAIL_API_KEY
elasticemailDailyLimit=ELASTICEMAIL_DAILY_LIMIT_FOR_FREETIER
passwordCallbackUrl=https://www.example.com
senderEmail=SYSTEM_EMAIL_SENDER_EMAIL
```

Step 3, install all dependencies for ExpressJS

```console
cd backend && yarn install
```

Step 4, install all dependencies for ReactJS

```console
cd frontend && yarn install
```

Step 5, create your own config.js in **frontend/src** directory with following settings:

```javascript
const config = {
  apiDomain: "API_DOMAIN",
  accessTokenKey: "THE_KEY_FOR_LOCAL_STORAGE_TO_STORE_ACCESS_TOKEN",
  googleApiKey: "GOOGLE_API_KEY",
  mediaFileDomain: "http://localhost:8080", //If you allow images to be uploaded to your local server
  saveMediaFileLocal: false, //Set this to true if you allow images to be uploaded to your local server
  sendgridApiKey: "SENDGRID_API_KEY",
  sendgridDailyLimit: "SENDGRID_DAILY_LIMIT_FOR_FREETIER",
  elasticemailApiKey: "ELASTICEMAIL_API_KEY",
  elasticemailDailyLimit: "ELASTICEMAIL_DAILY_LIMIT_FOR_FREETIER",
  passwordCallbackUrl: "https://www.example.com",
  senderEmail: "SYSTEM_EMAIL_SENDER_EMAIL"
};

export default config;
```

Step 6, set up database

Before run the following command, make sure you already created a database and have it configured in your **.env** file.

```console
cd server && yarn db:migrate
```


## How to run this?

```console
cd client && yarn start
```

## Unit Test

For every main directory (components, containers etc.), there should be a \_\_tests\_\_ directory for all unit test cases.

```console
cd clint && yarn test [test_directory]
cd server && yarn test [test_directory]
```

For styling below command should be used.

```console
yarn lint:client
````
