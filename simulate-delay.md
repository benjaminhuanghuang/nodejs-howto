## Simulate delay to all requests

```
// use middleware simulate latency
app.use(function(req,res,next)
{
  setTimeout(next,3000)
});
```

