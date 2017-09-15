Node 8
Sample 1
```
const { promisify } = require('util');
const delay = promisify(setTimeout);

delay(3000).then(()=>console.log('done'));
```

Sample 2
```
const { promisify } = require('util');
const readFile = promisify(fs.readFile);

readFile('./test.js', 'utf-8').then(content => console.log(content));
```