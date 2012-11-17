# DeviceMotionEvent - Demo
This is a demo of the devicemotion event API as defined by [W3C](http://dev.w3.org/geo/api/spec-source-orientation.html#devicemotion).

## What does the demo do?
The demo uses the devicemotion event API to collect sensor data from the accelerometer and gyroscope on the iPhone. The data is sent to a mirror-server using websockets. The following properties are then plotted against time: <code>.accelerationIncludingGravity</code>, <code>.rotationRate</code>, <code>.acceleration</code>.

+ The demo is built to run with Chrome on Mac OSX Mountain Lion and an iPhone 4. I haven't extensively tested it on other browsers or devices, but it should still work… let me know how you go [@hadi_michael](http://www.twitter.com/hadi_michael).
+ Both devices need to share the same wireless network.
+ Port :3000 should not be blocked by your router or firewall - if it is, modify server.js to listen on a different (available) port.

## Setup
You will need [node.js](http://www.nodejs.org), [express](http://expressjs.com/) and [socket.io](http://socket.io/) for this demo.

1. Download and install node.js from: [http://nodejs.org/](http://nodejs.org/).
2. Once you have node, use the "node package manager" in terminal to install "express" using <code>$ npm install express</code> and "socket.io" using <code>$ npm install socket.io</code>.

### Read about the packages used:
+ express: [https://npmjs.org/package/express](https://npmjs.org/package/express)
+ socket.io: [https://npmjs.org/package/socket.io](https://npmjs.org/package/socket.io)

+ This demo also uses [jQuery](http://jquery.com/) and [jQuery.flot](http://www.flotcharts.org/).

## Running the demo
1. In terminal, start the server: <code>$ node /path/to/server.js</code>
2. In Chrome, navigate to: <code>http://localhost:3000</code> - if you have replaced the port number in server.js, then replace it here as well.
3. Connect to the server in Safari on your iPhone by navigating to <code>my.macs.ip.address:3000</code>. If you're on a small local home network, it is likely that your IP address will be something like <code>192.168.0.1</code>. If you don't know it, use <code>$ ifconfig</code> to get it.

# LICENSE (MIT)
Copyright (C) 2012 Hadi Michael

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.