## Create middle
```
app.use(function(req,res,next)
{
   // do something
});
```

## Apply middleware to all request
```
app.use(bodyParser.json());
```


## Apply middleware on routes
```
app.use('/api', bodyParser.json());
```

