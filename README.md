# ardyh-streamer

A websockat server to recieve a video stream from a Raspberry Pi

0. Install dependaency
```
npm install ws
```


1. Start the server
```
node stream-server.js <password>
```

2. On raspberry pi run 
```
ffmpeg -s 320x240 -f video4linux2 -i /dev/video1 -f mpeg1video -b 800k -r 30 http://<domain>:8082/<password>/320/240/
```
