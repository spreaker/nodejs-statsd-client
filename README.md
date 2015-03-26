# Node.js Statsd Client


### How to install

``` bask
npm install node-statsd-client
```


### How it works

``` js
var Client = require('node-statsd-client').Client;

var client = new Client("localhost", 8192);

// Count stat
client.count("num_logged_users", 1);
client.increment("num_logged_users");
client.decrement("num_logged_users");

// Timing stat
client.timing("request_ms", 250);

// Gauge stat
client.gauge("gauge_stats", 4);
```


### Changes

#### 1.0.3 (2015-03-26)
 * Added LICENSE (BSD)
 * Updated README

#### 1.0.2 (2013-01-17)
 * Removed unnecessary "underscore" dependency (thanks to omega)

#### 1.0.1 (2012-06-21)
 * Fixed global leak of Client (thanks to sreuter)

#### 1.0.0 (2012-06-07)
 * This is the 3rd statsd client for node.js. I don't like to re-invent the wheel and
   I must admint it's really a bad thing. However, I need a simple but working statsd
   client and it seems that (at the time of writing) the other modules suffer small
   bugs that prevent me to put it in production. Now you know cause there're 3 modules
   for such a simple client.


### Contributors

 * [sreuter](https://github.com/sreuter)
