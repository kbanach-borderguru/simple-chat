Simple Chat
===========


## Install on Ubuntu

```
npm install
sudo apt-get install redis-server
sudo nano /etc/redis/redis.conf        
```

In `nano` you should add those two lines in very bottom of the file:

```
maxmemory 128mb
maxmemory-policy allkeys-lru
```

and then

```
sudo systemctl restart redis-server.service  
```

## Running 

```
node index.js 8080
```

Note: Second parameter (here it's `8080`) is port on which server will run
You can run multiple servers on different ports

## Connecting from browser

Running server is available under http://localhost:8080/ 

Open few different browsers and connect nodes running on few different ports, like 

```
node index.js 8080 // will be available under http://localhost:8080/
node index.js 8081 // will be available under http://localhost:8081/
node index.js 8082 // will be available under http://localhost:8082/
```

