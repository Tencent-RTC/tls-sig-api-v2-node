## Note
This Node project implements Tencent-RTC's UserSig authentication, providing a secure server-side method for generating signatures to protect the keys from leakage.

![](https://cloudcache.intl.tencent-cloud.com/cms/backend-cms/12569f72920411ef810152540055f650.png)

## npm integration
```shell 
npm i tls-sig-api-v2
```

## source code integration
Just place the file `TLSSigAPIv2.js` in the desired path.

## interface call
```javascript
var TLSSigAPIv2 = require('tls-sig-api-v2');
// var TLSSigAPIv2 = require('./TLSSigAPIv2'); // Source code integration uses relative paths

var api = new TLSSigAPIv2.Api(1400000000, "5bd2850fff3ecb11d7c805251c51ee463a25727bddc2385f3fa8bfee1bb93b5e");
var sig = api.genSig("xiaojun", 86400*180);
console.log(sig);
```
