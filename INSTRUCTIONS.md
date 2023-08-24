# Private Blockchain Application

Simple Private Blockchain with Blocks in Node.js and JavaScript that will be validated before adding into chain.

## What tools or technologies are used in this application?

- This application will be created using Node.js and Javascript programming language. The architecture will use ES6 classes
  because it will help us to organize the code and facilitate the maintnance of the code.
- The company suggest to use Visual Studio Code as an IDE to write your code because it will help you debug the code easily
  but you can choose the code editor you feel confortable with.
- Some of the libraries or npm modules you will use are:
  - "bitcoinjs-lib": "^4.0.3",
  - "bitcoinjs-message": "^2.0.0",
  - "body-parser": "^1.18.3",
  - "crypto-js": "^3.1.9-1",
  - "express": "^4.16.4",
  - "hex2ascii": "0.0.3",
  - "morgan": "^1.9.1"
    Remember if you need install any other library you will use `npm install <npm_module_name>`

Libraries purpose:

1. `bitcoinjs-lib` and `bitcoinjs-message`. Those libraries will help us to verify the wallet address ownership, we are going to use it to verify the signature.
2. `express` The REST Api created for the purpose of this project it is being created using Express.js framework.
3. `body-parser` this library will be used as middleware module for Express and will help us to read the json data submitted in a POST request.
4. `crypto-js` This module contain some of the most important cryotographic methods and will help us to create the block hash.
5. `hex2ascii` This library will help us to **decode** the data saved in the body of a Block.

### Starting:

Open a terminal and run the command `npm install`

Quickly check if the Node is running the app `node app.js`

You should see in your terminal the the Express application is listening in the PORT 8000

## How to test the application functionalities?

To test the application it is recommend you to use POSTMAN, this tool will help you to make the requests to the API.

1. Run your application using the command `node app.js`
   You should see in your terminal a message indicating that the server is listening in port 8000:

   > Server Listening for port: 8000

2. To make sure your application is working fine and it creates the Genesis Block you can use POSTMAN to request the Genesis block:
   ![Request: http://localhost:8000/block/0 ](https://s3.amazonaws.com/video.udacity-data.com/topher/2019/April/5ca360cc_request-genesis/request-genesis.png)
3. Make your first request of ownership sending your wallet address:
   ![Request: http://localhost:8000/requestValidation ](https://s3.amazonaws.com/video.udacity-data.com/topher/2019/April/5ca36182_request-ownership/request-ownership.png)
4. Sign the message with your Wallet:
   ![Use the Wallet to sign a message](https://s3.amazonaws.com/video.udacity-data.com/topher/2019/April/5ca36182_request-ownership/request-ownership.png)
5. Submit your Star
   ![Request: http://localhost:8000/submitstar](https://s3.amazonaws.com/video.udacity-data.com/topher/2019/April/5ca365d3_signing-message/signing-message.png)
6. Retrieve Stars owned by me
   ![Request: http://localhost:8000/blocks/<WALLET_ADDRESS>](https://s3.amazonaws.com/video.udacity-data.com/topher/2019/April/5ca362b9_retrieve-stars/retrieve-stars.png)
