Use bodyParser to extract the data 
```
app.use(bodyParser.json());  //parse json data and put it into req.body
app.use(bodyParser.urlencoded({extended: false}));
```

In the routes, use req.params and req.body to read data
```
router.get('/message/:msg', function (req, res, next) {
    res.render('node', {message: req.params.msg});
});

router.post('/message', function(req, res, next) {
    var message = req.body.message;
    res.redirect('/message/' + message);
});

```