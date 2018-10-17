Watson Speech JavaScript SDK Examples
=====================================

This folder has example Node.js and Python servers to generate auth tokens and 
several html files (in `static/`) with different examples of using the Speech SDK. 

There are also a few audio files to test with in the `static/` folder.


Prerequisite
------------

* IBM Watson Speech to Text service credentials - see [Service credentials for Watson services](https://www.ibm.com/watson/developercloud/doc/common/getting-started-credentials.html)
* Node.js OR Python
* [Bower](https://bower.io/) for installing client-side dependencies


Setup - Node.js
---------------

1. run `npm install` to grab dependencies (this automatically runs `bower install`)
2. create a `.env` file, with the following entries (entering the appropriate values):
  `SPEECH_TO_TEXT_APIKEY=`
  `SPEECH_TO_TEXT_URL=`
3. run `npm start`
4. Open your browser to http://localhost:3000/ to see the examples.


Notes
-----

* The examples all use [fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) (a modern promise-based replacement for XMLHttpRequest) to retrieve auth tokens. Most supported browsers include a native fetch implementation, but a pollyfill is included in the top-level module for older browsers.
* The examples use a Node.js server to generate tokens. It doesn't have to be written in Node.js, but *some server-side token generator is required*. The SDK will not accept your service credentials directly, and you can not use them to generate a token client-side. SDKs are available for [Node.js](https://github.com/watson-developer-cloud/node-sdk#authorization), [Java](https://github.com/watson-developer-cloud/python-sdk/blob/master/examples/authorization_v1.py), and there is a [REST API](https://www.ibm.com/watson/developercloud/doc/common/getting-started-tokens.html) for use with other languages (or `curl`).
* The Speech SDK may be used in browserify, Webpack, or as a standalone library. Most of the examples use the standalone version either installed via bower or symlinked to the root directory when developing locally.


More Examples
-------------

* Speech to Text: [Demo](https://speech-to-text-demo.mybluemix.net/), [Code](https://github.com/watson-developer-cloud/speech-to-text-nodejs)
* Speech & Dialog services together: [Demo](https://speech-dialog.mybluemix.net/), [Code](https://github.com/nfriedly/speech-dialog)
* Text to Speech w/ word timings: [Demo](http://watson-tts-timing.mybluemix.net/), [Code](https://github.com/nfriedly/tts-timing)
