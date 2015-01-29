# Phone Parser

An example node module that parses U.S. phone numbers.


## Use

```javascript
var Phone = require('phone-parser');

// Pretty print
var myNumber = new Phone("1234567890");
myNumber.toString();
// returns "(123) 456-7890"

// Area Code, Prefix, Suffix
var myNumber = new Phone("1234567890");
myNumber.areaCode();
// returns "123"
myNumber.numPrefix();
// returns "456"
myNumber.numSuffix();
// returns "7890"

// Remove leading 1
var myNumber = new Phone("11234567890");
myNumber.number();
// returns "1234567890"

// Clean dots from number
var myNumber = new Phone("123.456.7890");
myNumber.number();
// returns "1234567890"

// Returns zeros when invalid
var myNumber = new Phone("2.123.456.7890");
myNumber.number();
// returns "0000000000"


## Test

`npm install && npm test`
