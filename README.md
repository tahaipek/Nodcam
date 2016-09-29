# Nodcam
Access and stream web camera in **nodejs** using **ffmpeg**, **websockets** and **HTML5**.

###**Usage:**

```npm
$ git clone https://github.com/tahaipek/Nodcam.git

$ npm install

$ npm run express-server 
(Web server - node index.js)
	
$ npm run streaming-server 
(Web Sockets - node stream.js <secretKey>)
	
$ npm run ffmpeg 
(Streaming camera ffmpeg command => ffmpeg -f vfwcap -video_size 640x480 -framerate 24 -i video='<cameraDeviceName>':audio='<audioDeviceName>' <outputName>.mp4 -movflags faststart -framerate 15 -vcodec mpeg1video -preset veryfast -maxrate 3000k -bufsize 4000k -c:a aac -b:a 160k -ar 44100 -b:a 128k -f mpeg1video http://localhost:<webSocketsStreamingPort>/<secretKey>/<width>/height)
```


###**Third Party Libraries:**
  * **ExpressJs** http://expressjs.com/
  * **Ws** https://www.npmjs.com/package/ws
  *  **JsMpg** *(MPEG1 Video Decoder in JavaScript)* https://libraries.io/bower/jsmpg 

###**Requirements**
  * **NodeJs**
  * **ffmpeg** https://www.ffmpeg.org/


This application has been tested Windows 10. 

![preview.png](https://raw.githubusercontent.com/tahaipek/Nodcam/master/preview.png)
