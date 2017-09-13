## Connect to database
```
npm i mongoose -S
```

```
const mongoose = require('mongoose');

mongoose.Promise = global.Promise; // tell mongoose use Promise provide by node.js
mongoose.connect('mongodb://localhost:27017/test-db', {useMongoClient: true});

```

## Schema 1
```
const mongoose = require('mongoose');

const entitySchema = new mongoose.Schema({

});

// Define indexes
entitySchema.index({
    name: 'text',
    description: 'text'
});

// pre-save hook in mongo db
// Because we want to use this in the function, so don't use => function here
entitySchema.pre('save', async function (next) {
    // Do something
    next();
});

entitySchema.statics.getTagsList = function () {
    
}

module.exports = mongoose.model('Entity', entitySchema);
```

## Schema 2
```
const mongoose = require('mongoose');
const Schema = mongoose.Schema;

const entitySchema = new Schema({

});
```
## Schema 3
```

```

## Validator
var mongooseUniqueValidator = require('mongoose-unique-validator');

var userSchema = new Schema({
    firstName: {type: String, required: true},
    lastName: {type: String, required: true},
    password: {type: String, required: true},
    email: {type: String, required: true, unique: true},
    messages: [{type: Schema.Types.ObjectId, ref: 'Message'}]
});

userSchema.plugin(mongooseUniqueValidator);


## Reference
```
var userSchema = new Schema({
    firstName: {type: String, required: true},
    lastName: {type: String, required: true},
    password: {type: String, required: true},
    email: {type: String, required: true, unique: true},
    messages: [{type: Schema.Types.ObjectId, ref: 'Message'}]
});

var messageSchema = new Schema({
  content: { type: String, required: true },
  user: { type: Schema.Types.ObjectId, ref: "User" }
});
```


