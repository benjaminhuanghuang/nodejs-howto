## Method 1.
app.js
```

```


## Method 2.
/routes/apiRoutes
```
const aipRouter = express.Router();

apiRouter.route('/widgets')
    .get(function (req, res) {
    })
    .post(function (req, res) {
    });

```

app.js
```
const apiRouter = require('./routes/api');
app.use('/api', apiRoutes;
```
