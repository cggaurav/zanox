Zanox API written in Javascript
=================================

This is an Api to access [Zanox](http://www.zanox.com/) with nodejs.

Installation
------------

    npm install zanox_js

See /examples for usage
------------

This example gives you the sales as of 2013-05-20

```
var zanox_req, params, zanox;

zanox_req = require('zanox_js');

zanox = zanox_req(API_KEY, SHARED_SECRET);

params = {
  datetype: 'modifiedDate',
  state: 'approved'
};

zanox.getAllSalesOfDate('2013-05-20', params, function(err, data) {
  if (err != null) {
    return console.log('error', err);
  }
  return console.log('%j', data);
});
```

Thanks to [zanox](https://npmjs.org/package/zanox)
