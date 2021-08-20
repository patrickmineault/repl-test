# repl-test

Development notes: thebe runs over secure websockets, which means this page must be served through https to test live code locally. Generate a self-signed certificate with OpenSSL as such:



```
[dev]
[dev.https]
dir = _build/html
certFile = "cert.pem"
keyFile = "key.pem"
```