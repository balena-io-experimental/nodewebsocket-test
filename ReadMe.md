# nodewebsocket-test

A basic Node.js websocket server, to test resin proxy websocket functionality,
through the device Public URL.

## Testing

1. Install this application a resin device
2. Enable public URL
3. Use an online echo test, such as [this one by websocket.org](https://www.websocket.org/echo.html), connect to `wss://<UUID>.resindevice.io`, and send a message. The response should be `Server received from client: <message you sent>`.
4. Alternatively can use `wscat`: install it with `npm install wscat`, and run it from `node_modules/wscat/bin` as `./wscat --connect wss://<UUID>.resindevice.io`.
5. `wscat` is also installed on the devic, for local testing connect by `resin ssh <UUID>`, and from `/usr/src/app/node_modules/wscat/bin` run `./wscat --connect ws://localhost` (note, here it's `ws` as it is unsecured, as opposed to going through the proxy and connecting to secured `wss`).