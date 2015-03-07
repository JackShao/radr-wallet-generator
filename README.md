## Radr Wallet Generator

This is a simple, lightweight tool to generate a new radr wallet,
which consists of public and secret key components.

Beyond portability, the tool was created to isolate the cryptography
behind wallet generation in the radr client and radr-lib.

### Usage

  ```js
  var radrLib = require('radr-lib');
  var radrWallet = require('radr-wallet')({
    sjcl: radrLib.sjcl
  });

  radrWallet.generate();
  ```
    
will generate a random, unfunded Radr address and secret.

  ```js
  { 
    address: 'r3sBHwjwAb6eFpHbCEbJmhC8scmDeqXZyZ',
    secret: 'snovmDoPbb5Y14JVA5wxtBtPgHNaP' 
  }
  ```

### Tests

Run the automated test suite, which uses test vectors from the wiki:

    npm test

### Algorithm Docs and Test Vectors

A description of the Cryptography can be found on the [Wiki](https://wiki.radr.biz/Account_Family).