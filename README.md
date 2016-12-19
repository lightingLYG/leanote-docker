# lenote-docker

### How to run
#### 1. modify app.conf
The configurations of leanote is stored in the file leanote/conf/app.conf.

One setting that you are strongly suggested to modify is app.secret, please change arbitrary number of digits of the string to something different, but keeping the string length unchanged. This is to avoid potential security issues. 
```

db.host=127.0.0.1
db.port=27017

app.secret=V85ZzBeTnzpsHyjQX4zukbQ8qqtju9y2aDM55VWxAH9Qop1apoekx3xkcDVvrD0y #

```
#### 2. run leanote
```
docker run -d -p 9000:9000 -v /your_conf_path:/usr/local/src/leanote/conf/app.conf  lightinglyg/leanote:2.1-alpine
```
eg. 
```
docker run -d -p 9000:9000 -v /home/soft/leanote/conf/app.conf:/usr/local/src/leanote/conf/app.conf  lightinglyg/leanote:2.1-alpine
```
