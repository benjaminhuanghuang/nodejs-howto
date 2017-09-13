## Allow Cross Origin Request
  -https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS
  
  A resource makes a cross-origin HTTP request when it requests a resource from a different domain, protocol, or port to its own. 

```
app.use(function (req, res, next) {
    res.setHeader('Access-Control-Allow-Origin', '*');
    res.setHeader('Access-Control-Allow-Headers', 'Origin, X-Requested-With, Content-Type, Accept');
    res.setHeader('Access-Control-Allow-Methods', 'POST, GET, PATCH, DELETE, OPTIONS');
    next();
});
```