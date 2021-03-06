Springle Chat
=============

Realtime chat using NodeJS and WebSocket

Demo at https://sky.rebugged.com/ (Running version 0.4.3)

(<i>Demo shown at the above link might not reflect the latest changes in code</i>)

## Tech Stack
* WebSocket API (for establishing and maintaining socket connection with the server)
* NodeJS (acts as server and provides evented request handling)
* websocket module for NodeJS (provides support for WebSocket protocol in server.
* Apache (for serving static content)

## Languages
* Javascript

## Database
NIL

## Dependencies
* [Node.js](http://nodejs.org/) (Server side)
* [websocket module](https://github.com/Worlize/WebSocket-Node) for node (Server side)
* [Apache](http://httpd.apache.org/) web server to serve static contents (Server side)
* A [websocket compliant](http://caniuse.com/websocket) browser (Client side)

## How to use
* Install all the dependencies listed above (NodeJS, Websocket module, Apache server and a compliant browser)
* Clone/copy the Springle-Chat repsitory to a directory inside Apache's web root.
* In `js/chat_client.js`, set `var server_url` to your server URL (probably `localhost`). Leave the ports as is.
* In `js/chat_client.js`, set `var enable_ssl` value to `false`.
* In `js/server.js`, add your server URL (eg: `locahost`, `chat.your-server.com`) to `var allowed_origins` array.
* Open terminal and CD to the directory where Springle-Chat source code is extracted/cloned.
* Start chat server by typing `node js/server.js`
* Doing the above step will start the chat server, which will listen for incoming client connections.
* Browse to the source directory in your browser. (eg: http://localhost/Springle-Chat/) and you will get the chat login page.
* Login to chat giving any nickname and chat room name. Thats all!

### To enable SSL
 * Set the path to your SSL cert and key file in array `options.cert` and `options.key` in `js/server.js`
 * In `js/chat_client.js`, set `var enable_ssl` value to `true`.
 * Start chat server with ssl option as `node js/server.js --enable-ssl`
 * Open chat login page in browser also over HTTPS. (eg: https://localhost/Springle-Chat/)
 * Thats all!

### Troubleshooting Tips
 * Changes you make to the source files will not reflext in the chat front end. To effet the changes, you need to clear the 'HTML5 App Cache' in the browser. (Not normal cache, so `CTRL`+`F5` won't hellp.)
 * If chat is not connecting, open `Net` panel in Firebug and check what the error message shown there is.

## Change Log

###v0.4.3
New features
* Added facility to detect when connection is closed and ability to automatically reconnect. ([#14](https://github.com/riverspirit/Springle-Chat/issues/14))

###v0.4.2.1
Bug fix
* Now desktop notification code is invoked only after browser support for it is checked.

###v0.4.2
New features
* Direct links to chatrooms
* Desktop notifications for new messages (when chat window not in focus). ([#16](https://github.com/riverspirit/Springle-Chat/issues/16))

###v0.4.1
New features
* SSL support for Websocket communication

###v0.4
New Features
* Added facility to create and join chat rooms ([#5](https://github.com/riverspirit/Springle-Chat/issues/5))
* Some improvisions in fonts used.

###v0.3
New Features
* Sound notification for chat ([#4](https://github.com/riverspirit/Springle-Chat/issues/4))
* Convert to installable HTML5 web app ([#13](https://github.com/riverspirit/Springle-Chat/issues/13))

Fixes
* Prevent users from sending empty messages ([#10](https://github.com/riverspirit/Springle-Chat/issues/10))
* Do not strip away newline characters from messages ([#12](https://github.com/riverspirit/Springle-Chat/issues/12))

###v0.2
New Features
* New and improved UI.
* 'User is typing...' status message ([Ticket #1](https://github.com/riverspirit/Springle-Chat/issues/1))
* Show flashing title bar when there is new activity in the chat page. ([#2](https://github.com/riverspirit/Springle-Chat/issues/2))
* Bug fix: HTML tags in user input are stripped prior to rendering. ([#3](https://github.com/riverspirit/Springle-Chat/issues/3))
* Link to clear chat history.

###v0.1
Features
* Basic functional system with multi-user chat

## License
Source code is released under GNU Affero General Public License v3. See included file `license.txt` for details.




