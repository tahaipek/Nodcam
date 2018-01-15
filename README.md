# Nodcam
Access and stream web camera in **nodejs** using **ffmpeg**, **websockets** and **HTML5**.

### **Usage:**

```npm
$ git clone https://github.com/tahaipek/Nodcam.git

$ cd Nodcam

$ npm install

$ npm run express-server
(Web server - node index.js)
	
$ npm run streaming-server
(Web Sockets - node stream.js <secretKey>)
	
$ npm run ffmpeg
(Streaming camera ffmpeg command => 
ffmpeg -f dshow -i video="<cameraDeviceName>":audio="<audioDeviceName>" <outputName>.mp4 -f mpeg1video http://localhost:<webSocketsStreamingPort>/<secretKey>/<width>/height)
if you don't want to record, remove 'output' keyword.
```


### **Third Party Libraries:**
  * **ExpressJs** http://expressjs.com/
  * **Ws** https://www.npmjs.com/package/ws
  *  **JsMpg** *(MPEG1 Video Decoder in JavaScript)* https://libraries.io/bower/jsmpg 

### **Requirements**
  * **NodeJs** https://nodejs.org/
  * **ffmpeg** https://www.ffmpeg.org/


This application has been tested Windows 10. 

![preview.png](https://raw.githubusercontent.com/tahaipek/Nodcam/master/preview.png)
