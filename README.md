

### MemViz - Express middleware for visualizing memory usage


##### <i> install </i>:  `npm install memviz -S`


### Usage 

```js
const express = require('express');
const {memviz} = require('memviz');

const app = express();

app.use('/memory', memviz({
  frequency: 100,  // sample interval (in seconds)
  maxCount: 200000,  // maximum number of entries to store
  maxAge: 4000000   // only keep entries young than this 
}));
```


If you make a `GET /memory` request to your server, you will see this in the browser:

<kbd>
    <img src="https://raw.githubusercontent.com/oresoftware/memviz/master/media/memviz.png">
</kbd>

You can probably use an iframe to display this on a webpage as well.


