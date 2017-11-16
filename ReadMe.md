# nodewebsocket-test

A basic Node.js websocket server, to test resin proxy websocket functionality,
through the device Public URL.

## Testing

1. Install this application a resin device
2. Enable the [Public Device URl URL](https://docs.resin.io/management/devices/#enable-public-device-url)
4. You can use `wscat` to test: install it with `npm install wscat`, and run it from `node_modules/wscat/bin` as `./wscat --connect wss://<UUID>.resindevice.io`.
5. `wscat` is also installed on the devic, for local testing connect by `resin ssh <UUID>`, and from `/usr/src/app/node_modules/wscat/bin` run `./wscat --connect ws://localhost` (note, here it's `ws` as it is unsecured, as opposed to going through the proxy and connecting to secured `wss`).

Note: before could use an online echo test, such as the [Kaazing WebSocket Echo Demo](http://demos.kaazing.com/echo/), to connect to `wss://<UUID>.resindevice.io` and send a message. However that doesn't seem to work at the moment, as the demo does not seem to do the "Upgrade" step of the protocol. The response should have been `Server received from client: <message you sent>`.

## License

Copyright 2017 Resinio, Ltd.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
