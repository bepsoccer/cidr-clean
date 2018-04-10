# cidr-clean
-----------
[![Build Status](https://travis-ci.org/bepsoccer/cidr-clean-bp.svg?branch=master)](https://travis-ci.org/bepsoccer/cidr-clean-bp)
[![MIT Licence](https://badges.frapsoft.com/os/mit/mit.svg?v=103)](https://opensource.org/licenses/mit-license.php)

What for ?
----------

Clean an array of CIDR
* remove duplicates
* remove comments
* remove bad CIDRs
* remove extra spaces
* choose the heaviest network in case of overlap

This is a fork of cidr-clean by Eviltik to make it work with an older nodejs implementation.

Installation
------------
```
$ npm install cidr-clean-bp
```


Usage
-----
```
const cidrClean = require('cidr-clean-bp');

let list = [
    '#mycomment',
    '10.1.2.0/23',
    '110.1.3.248/30',
    '1.2.3.4/10'
];

console.log(cidrClean(list));

# output: ['10.1.2.0/23', '110.1.3.248/30', '1.2.3.4/10'];

# note, you can cidrClean(list1, list2) for merging 2 cidr lists
```

Todo
----
* optional callback with all events (remove, overlap)
