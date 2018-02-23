![KOACH](https://github.com/SystangoTechnologies/Koach/blob/master/static/koach.png)

## KOACH
Production ready boilerplate for building APIs with [koa2](https://github.com/koajs/koa/), sequelize and http/2 as the communication protocol.

## Description
This project covers basic necessities of most APIs.
* Authentication (passport & jwt)
* Database (SQL)
* Testing (mocha)
* http/2 support for websites and apis
* Doc generation with apidoc
* linting using standard
* Contains two versions of API

Please note, if you are planning to use this boilerplate for creating a web application then the 'https' protocol should be used to access its pages.

Visit `https://localhost:3000/` to access the root page.

## Requirements
* node > v8.9.4
* SQL Database

## Installation
```bash
git clone https://github.com/SystangoTechnologies/Koach-SQL.git
```

## Features
* [koa2](https://github.com/koajs/koa)
* [koa-router](https://github.com/alexmingoia/koa-router)
* [koa-bodyparser](https://github.com/koajs/bodyparser)
* [koa-generic-session](https://github.com/koajs/generic-session)
* [koa-logger](https://github.com/koajs/logger)
* [koa-helmet](https://github.com/venables/koa-helmet)
* [koa-convert](https://github.com/koajs/convert)
* [Sequelize](https://github.com/sequelize/sequelize)
* [http/2](https://github.com/molnarg/node-http2)
* [Passport](http://passportjs.org/)
* [Nodemon](http://nodemon.io/)
* [Mocha](https://mochajs.org/)
* [apidoc](http://apidocjs.com/)
* [Babel](https://github.com/babel/babel)
* [ESLint](http://eslint.org/)
* [Gulp](https://github.com/gulpjs/gulp/)
* [PM2](https://github.com/Unitech/pm2/)
* [Swagger](https://github.com/swagger-api/)

## Structure
```
├── bin
│   └── server.js                   # Bootstrapping and entry point
├── cert
│   ├── server.cert                 # SSL certificate
│   └── server.key                  # SSL certificate key
├── config                          # Server configuration settings
│   ├── env                         # Environment specific config
│   │   ├── common.js
│   │   ├── development.js
│   │   ├── production.js
│   │   └── test.js
│   ├── index.js                    # Config entrypoint
│   └── passport.js                 # Passportjs config of strategies
├── src                             # Source code
│   ├── modules                     # Module-specific controllers
│   │    ├── common                 # Contains common modules
│   │    │   ├─── home              
│   │    │   └─ index.js
│   │    ├── v1                     # Version v1 of APIs
│   │    │   ├─ Auth
│   │    │   ├─ User   
│   │    │   └─ index.js            
│   │    └─── v2                     # Version v2 of APIs
│   │         ├─ Auth
│   │         ├─ User   
│   │         └─ index.js
│   ├── models                      # Sequelize models
│   │   ├── index.js                # Creates connection from database and load models
│   │   └── user.js                 # User model
│   └── middleware                  # Custom middleware
│       └── validators              # Validation middleware
└── test                            # Unit tests
```

## Usage
* `gulp prod` Start server on production mode with PM2
* `gulp` Start server on development mode with nodemon
* `npm run docs` Generate API documentation
* `npm test` Run mocha tests

## Database
##### And one of the following databases with Sequelize:
* npm install --save pg pg-hstore
* npm install --save mysql2
* npm install --save sqlite3
* npm install --save tedious

## Environment Variables
* SESSION
* TOKEN
* DATABASE
* DB_USERNAME
* DB_PASSWORD
* DB_HOST
* DB_DBPORT
* DB_DIALECT

## Documentation
API documentation is written inline and generated by [apidoc](http://apidocjs.com/).

Visit [https://localhost:3000/docs/](https://localhost:3000/docs/) to view docs

To view swagger API documentation

Visit [https://localhost:3000/swagger](https://localhost:3000/swagger) to view Swagger UI.

## Performance Comparison
The environment for the test caes are following-
* Node Version: **8.9.4**
* Number of Users: **1500**
* Ramp-up Period: **300 seconds**
* Loop Count: **100**

![Average](https://raw.githubusercontent.com/SystangoTechnologies/Koach/master/static/Average.png)
![Throughput](https://github.com/SystangoTechnologies/Koach/raw/master/static/Throughput.png)

## Contributors
[Arpit Khandelwal](https://github.com/arpit-systango)
[Anurag Vikram Singh](https://github.com/avsingh-systango)

## License
MIT.