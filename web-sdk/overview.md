---
id: web-sdk
title: Symbl Web SDK 
sidebar_label: Introduction
slug: /web-sdk/overview
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

---

The Symbl Web SDK provides access to the Symbl APIs from applications written in the JavaScript directly in the browser. It includes a pre-defined set of classes so you can easily utilize APIs.

> **Source Code** <br/>
Find the source code here: [https://github.com/symblai/symbl-web-sdk](https://github.com/symblai/symbl-web-sdk). <br/>

> For the Web SDK source code available in Labs, go here: [https://github.com/symblai/symbl-web-sdk/tree/labs](https://github.com/symblai/symbl-web-sdk/tree/labs).

## Supported Browsers

 |-- | Chrome | Edge Firefox | Firefox | Safari | 
 | -------| ---------- | ------- | ----- | ------- | 
 | macOS | ![icon](/img/tick-mark.png)| ![icon](/img/tick-mark.png)| ![icon](/img/tick-mark.png) | ![icon](/img/tick-mark.png) |
 | Windows | ![icon](/img/tick-mark.png) | ![icon](/img/tick-mark.png)| ![icon](/img/tick-mark.png) |  |
 | Linux | ![icon](/img/tick-mark.png)|   | ![icon](/img/tick-mark.png) |
 | iOS | ![icon](/img/tick-mark.png)|   | ![icon](/img/tick-mark.png) | ![icon](/img/tick-mark.png) |
 | Android | ![icon](/img/tick-mark.png)|  | ![icon](/img/tick-mark.png) | ![icon](/img/tick-mark.png) |
 
## Setup

To use the Symbl Web SDK, 

You can include it via script tags in your HTML file:

```html
<script src="https://storage.googleapis.com/symbl-web-sdk/latest/symbl.min.js"></script>
```
In case of a front-end web application using a framework such as React, import it in the ES2015 style:

```bash
import symbl from "@symblai/symbl-web-sdk";
```
:::note For Labs 

## Installation
`npm install @symblai/symbl-web-sdk@labs`

## Setup
n order to use the Symbl Web SDK you need to include it via script tags in your HTML file or in the case of a front-end web application using a framework such as React, import it in the ES2015 style.

**HTML script**

`<script src="https://storage.googleapis.com/symbl-web-sdk/latest-labs/symbl.min.js"></script>`

**Web Application import**

`import symbl from "@symblai/symbl-web-sdk";`
:::

## Initialization

The `init` authenticates you to use the Symbl API using the provided authentication credentials.

You can authenticate:

- [Using your API Credentials](#authenticate-using-api-credentials) 

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; or 

- [Using your Auth Token](#authenticate-using-token) 

### Authenticate using API Credentials

Use the code given below to authenticate using your Symbl App ID and App Secret. 

```js
sdk.init({
  // APP_ID and APP_SECRET come from the Symbl Platform: https://platform.symbl.ai
  appId: APP_ID,
  appSecret: APP_SECRET,
  basePath: 'https://api.symbl.ai'
})
.then(() => console.log('SDK Initialized.'))
.catch(err => console.error('Error in initialization.', err));
 ```

### Authenticate using Token 

Use the code given below to authenticate using the Auth Token. 

```js
sdk.init({
  accessToken: ACCESS_TOKEN_HERE,
  basePath: 'https://api.symbl.ai'
})
.then(() => console.log('SDK Initialized.'))
.catch(err => console.error('Error in initialization.', err));
```

## Tutorials

We have prepared a list of tutorials to help you understand how to use the Web SDK.

#### Streaming API Tutorials

* [Transcribing Live Audio Input through Microphone](/docs/web-sdk/transcribing-live-audio-through-microphone)


### Code Snippets

#### Streaming API Code Snippets

* [Subscribe to real-time Events](/docs/web-sdk/subscribe-real-time)
* [Reconnecting to an Existing Real-time Connection](/docs/web-sdk/reconnecting-real-time)
* [Muting and Unmuting the Connected Device](/docs/web-sdk/muting-and-unmuting-connected-device)
* [Stopping Real-time Connection](/docs/web-sdk/stopping-real-time)
* [Features in Labs](/docs/web-sdk/web-sdk-labs)


### JavaScript SDK Reference

Supported methods and events for the Symbl JavaScript SDK are listed below:

* [Public Endpoints](/docs/javascript-sdk/reference#public-methods)
    * [init](/docs/javascript-sdk/reference#init)
    * [startEndpoint](/docs/javascript-sdk/reference#startendpoint)
    * [stopEndpoint](/docs/javascript-sdk/reference#stopendpoint)
    * [startRealtimeRequest](/docs/javascript-sdk/reference#startRealtimeRequest)
    * [subscribeToConnection](/docs/javascript-sdk/reference#subscribetoconnection)
    * [pushEventOnConnection](/docs/javascript-sdk/reference#pusheventonconnection)
* [Event Handlers](/docs/javascript-sdk/reference#event-handlers-1)
    * [onSpeechDetected](/docs/javascript-sdk/reference#onspeechdetected)
    * [onMessageResponse](/docs/javascript-sdk/reference#onmessageresponse)
    * [onInsightResponse](/docs/javascript-sdk/reference#oninsightresponse)
    * [onTopicResponse](/docs/javascript-sdk/reference#ontopicresponse)

