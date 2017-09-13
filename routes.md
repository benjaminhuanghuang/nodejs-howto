## Method 1.
Set routes in app.js directly
```
app.use('/', (req, res)=>{

});
```

## Method 2, Using express.Router 
/routes/app.js
```
var express = require('express');
var router = express.Router();

router.get('/', function (req, res, next) {
    res.render('index');
});

module.exports = router;
```

app.js
```
var appRoutes = require('./routes/app');
app.use('/', appRoutes);
```

## Method 3
Add route to app in routes file
```
module.exports = app => {
  app.get("/auth/google", passport.authenticate("google", {
      scope: ["profile", "email"]
    })
  );
```

Call routes in app.js
```
require("./routes/authRoutes")(app);
```
