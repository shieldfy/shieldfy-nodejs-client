# Shieldfy NodeJs SDK - Beta

This is the official NodeJs SDK for Shieldfy (shieldfy.io) https://shieldfy.io

Shieldfy is a strong application protection platform that helps businesses to secure their applications online.

## Installation

1. You will first need to register on [shieldfy.io](https://shieldfy.io/) to get your APP Key & APP Secret.
2. install nodejs sdk package through NPM (recommanded)
    ```
    npm install shieldfy-nodejs-client
    ```

## Usage

### open `index.js` or (main file) and type the following:

`index.js` File
```js
const shieldfy= require('shieldfy-nodejs-client');
shieldfy.start({
    appKey:'yourAppKey',
    appSecret:'YourAppSecret',
});
```

### Or, in case using environment variable (`.env` File)

`index.js` File
```js
const shieldfy= require('shieldfy-nodejs-client')
shieldfy.start();
```

`.env` File
```js
shieldfyAppKey = "yourAppKey"
shieldfyAppSecret = "YourAppSecret"
```

### NOTE: You should require Shieldfy in the main file at first before any other package or module in order to SDK work correctly.


## Detection-Mode

### BLOCK

This is default mode in which if there exist attack on your application SDK will stop the attack and block it then report     to the shieldfy dashboard.


### LISTEN

In this mode the SDK will not bloack any attack but it will still report this attacks to shieldfy dashboard. 
to activate this mode pass action property equal "listen" in the object to the `shieldfy.start()` function as following
    
```js
const shieldfy= require('shieldfy-nodejs-client');
shieldfy.start({
    appKey:'yourAppKey',
    appSecret:'YourAppSecret',
    action: 'listen'
});
```


## Configuration

For more information about configurations and usage, refer to the official documentation at [docs.shieldfy.io](#).

## Contributing

Thank you for considering contributing to this project!
Bug reports, feature requests, and pull requests are very welcome.


## Security Vulnerabilities

If you discover a security vulnerability within this project, please send an e-mail to `security@shieldfy.com`.
