# Nodejs-basic-auth-token

```
                var tmp = auth.split(' ');   // Split on a space, the original auth looks like  "Basic Y2hhcmxlczoxMjM0NQ==" and we need the 2nd part

                var buf = new Buffer(tmp[1], 'base64'); // create a buffer and tell it the data coming in is base64
                var plain_auth = buf.toString();        // read it back out as a string

                console.log("Decoded Authorization ", plain_auth);

                // At this point plain_auth = "username:password"

                var creds = plain_auth.split(':');      // split on a ':'
                var username = creds[0];
                var password = creds[1];
                
```
