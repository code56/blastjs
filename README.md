# blast.js

## Library
### Install

```bash
npm install blastjs --save
```

### Usage
#### make database

```javascript
var blast = require('blastjs');

var type = 'prot';
var fileIn = './data.fasta';
var outPath = './';
var name = 'myDatabase';


blast.makeDB(type, fileIn, outPath, name, function(err){
  if(err){
    console.error(err);   
  } else {
    console.log('database created at', outPath);
  }
});
```

#### blast n
```javascript
var blast = require('blastjs');

var dbPath = './myDatabase';
var query = 'TGACTGACTGACTGACTGACTGAC';

blast.blastN(db, dbPath, function (err, output) {
  if(!err){
    console.log(output);
  }
});

```


## REST API + Web Interface
### Install
```bash
npm install -g blastjs
```

### Start
```bash
blastjs-server
```


## Desktop App
TODO