![Logo](https://github.com/posidron/posidron.github.io/raw/master/static/images/argus.png)

[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
[![Build Status](https://api.travis-ci.org/mozillasecurity/argus.svg?branch=master)](https://travis-ci.org/MozillaSecurity/argus) [![IRC](https://img.shields.io/badge/IRC-%23fuzzing-1e72ff.svg?style=flat)](https://www.irccloud.com/invite?channel=%23fuzzing&amp;hostname=irc.mozilla.org&amp;port=6697&amp;ssl=1)


### Prerequisites

[Redis](https://redis.io/download) and
[MongoDB](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/#install-mongodb-community-edition) are required.

```bash
brew install redis mongodb
```

### Setup Prerequisites

```bash
redis-sever
mongodb --dbpath=/tmp/
```

### Setup
```bash
npm install
```

### Development

```bash
npm run development

or

pm2 start server/server.js --watch
```

### API

| Type   | Path           | Description                |
| -------|:---------------| :--------------------------|
| GET    | /signup        | Register                   |
| POST   | /signin        | Retrieving the JWT         |
| GET    | /api/repos/    | Get a list of repositories |
| POST   | /api/repos     | Add a repository           |
| GET    | /api/repos/:id | Get commits                |
| DELETE | /api/repos/:id | Delete a repository        |
| PUT    | /api/repos/:id | Force pulling a repository |


The ```x-access-token``` header needs to be set in order to make a request to any API path. The JWT token can be obtained during the ```signin``` process.

### Testing

```bash
npm test
```
