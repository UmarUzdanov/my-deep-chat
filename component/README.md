<br />

![Deep Chat](../assets/readme/banner.png)

<b>Deep Chat</b> is a fully customizable chat based web component built with a focus on powering next generation AI services. Whether you want to create a chatbot that leverages popular APIs such as ChatGPT or you want to connect to your own custom service, this component can do it all! Explore [deepchat.dev](https://deepchat.dev/) to view all of the available features, how to use them, examples and more!

### :rocket: Main Features

- Connect to any API
- Avatars
- Names
- Send/Receive files
- Capture photos via webcam
- Record audio via microphone
- Speech To Text for message input
- Text To Speech to hear message responses
- Support for MarkDown to help structure text and render code
- Introduction panel and dynamic modals to help describe functionality for your users
- Connect to popular AI APIs such as OpenAI, HuggingFace, Azure directly from the browser
- Support for all major ui frameworks/libraries
- Everything is customizable!

### :computer: Getting started

```
npm install deep-chat
```

If using React, install the following instead:

```
npm install deep-chat-react
```

To test the component - simply add the following to your markup:

```
<deep-chat directConnection='{"demo":true}'/>
```

The exact syntax for the above example will vary depending on the framework of your choice ([see here](https://activetable.io/examples/frameworks)).

### :zap: Connect

![Connect](./assets/readme/connect.png)

Connecting to a service is simple, all you need to do is define its API details using the [`request`](https://deepchat.dev/docs/connect#request) property:

```
<deep-chat request='{"url":"https://service.com/chat"}'/>
```

The service will need to be able to handle request and response formats used in Deep Chat. Please read the [Connect](https://deepchat.dev/docs/connect) section in documentation and check out full [project examples](WORK).

Alternatively, if you want to connect without changing the target service, use the [`requestInterceptor`](https://deepchat.dev/docs/interceptors#requestInterceptor) and [`responseInterceptor`](https://deepchat.dev/docs/interceptors#responseInterceptor) properties to augment the incoming and outgoing request details.

### :electric_plug: Direct connection

![Direct connection](./assets/readme/direct-connect.png)

Connect to popular AI APIs directly from the browser via the use of the [`directConnection`](https://deepchat.dev/docs/directConnection/#directConnection) property:

```
<deep-chat directConnection='{"openAI":true}'/>

<deep-chat directConnection='{"openAI":{"key": "optional-key-here"}}'/>
```

Please note that this approach should be used for local/prototyping/demo purposes ONLY as it exposes the API Key to the browser. When ready to go live, please switch to using the [`request`](https://deepchat.dev/docs/connect#request) property described above with a combination of a [proxy service](https://github.com/OvidijusParsiunas/deep-chat/tree/main/example-servers).

Currently supported direct API connections:

| OpenAI                                                                                                                                                               | Cohere                                                                                                                                                         | Azure                                                                                                                                                                                        | HuggingFace                                                                                                                                                                                        | AssemblyAI                                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://openai.com/blog/openai-api" target="_blank"><img src="./website/static/img/openAILogo.png" width="45" style="display: block; margin: 0 auto;"/></a> | <a href="https://docs.cohere.com/docs" target="_blank"><img src="./website/static/img/cohereLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> | <a href="https://learn.microsoft.com/en-gb/azure/cognitive-services/" target="_blank"><img src="./website/static/img/azureLogo.png" width="52" style="display: block; margin: 0 auto;"/></a> | <a href="https://learn.microsoft.com/en-gb/azure/cognitive-services/" target="_blank"><img src="./website/static/img/huggingFaceLogo.png" width="57" style="display: block; margin: 0 auto;"/></a> | <a href="https://www.assemblyai.com/" target="_blank"><img src="./website/static/img/assemblyAILogo.png" width="39" style="display: block; margin: 0 auto;"/></a> |

### :camera: :microphone: Camera and Microphone

Use Deep Chat to capture photos with your webcam and record audio with the microphone.
![Capture](./assets/readme/capture.png)

You can enable this using the [`camera`](https://deepchat.dev/docs/files#camera) and [`microphone`](https://deepchat.dev/docs/files#microphone) properties:

```
<deep-chat camera="true" microphone="true" ...other properties />
```

### :microphone: :sound: Speech

![alt text](./assets/readme/title.png)

Input text with your voice using Speech To Text capabilities and have the responses read out to you with Text To Speech. You can enable this functionality via the [`speechToText`](HERE) and [`textToSpeech`](HERE) properties.

```
<deep-chat speechToText="true" microphone="textToSpeech" ...other properties />
```

### :beginner: Examples

Check out the live codepen examples for your [UI framework/library](https://deepchat.dev/examples/frameworks) of choice:

| React                                                                                                                                                                                              | Vue 2                                                                                                                                                                                           | Vue 3                                                                                                                                                                                           | Svelte                                                                                                                                                                                              | Angular                                                                                                                                                                                                               | Solid                                                                                                                                                                                                                    | Next                                                                                                                                                                                                                                                                                                                                                     | VanillaJS                                                                                                                                                                                                 |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://codesandbox.io/s/deep-chat-react-ythnyl?file=/src/App.tsx" target="_blank"><img src="./website/static/img/reactLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> | <a href="https://codesandbox.io/s/deep-chat-vue2-cdqpt2?file=/src/App.vue" target="_blank"><img src="./website/static/img/vueLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> | <a href="https://codesandbox.io/s/deep-chat-vue3-7y99jq?file=/src/App.vue" target="_blank"><img src="./website/static/img/vueLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> | <a href="https://codesandbox.io/s/deep-chat-svelte-832jcc?file=/App.svelte" target="_blank"><img src="./website/static/img/svelteLogo.png" width="45" style="display: block; margin: 0 auto;"/></a> | <a href="https://codesandbox.io/s/deep-chat-angular-mk2v62?file=/src/app/app.component.html" target="_blank"><img src="./website/static/img/angularLogo.png" width="66" style="display: block; margin: 0 auto;"/></a> | <a href="https://codesandbox.io/p/sandbox/deep-chat-solidjs-nnx9nc?file=%2Fsrc%2FApp.tsx%3A1%2C1" target="_blank"><img src="./website/static/img/solidLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> | <a href="https://codesandbox.io/p/sandbox/deep-chat-nextjs-pvyy5p?selection=%5B%7B%22endColumn%22%3A30%2C%22endLineNumber%22%3A28%2C%22startColumn%22%3A30%2C%22startLineNumber%22%3A28%7D%5D&file=%2Fpages%2Findex.tsx%3A13%2C30" target="_blank"><img src="./website/static/img/nextLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> | <a href="https://codesandbox.io/s/deep-chat-vanillajs-v2ywnv?file=/index.html" target="_blank"><img src="./website/static/img/vanillaJSLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> |

Browse the following example [server templates](WORK) to help complete your final chat architecture:

| Express                                                                                                                                                                                                                  | Nest                                                                                                                                                                                                                 | Flask                                                                                                                                                                                                                  | Spring                                                                                                                                                                                                                         | Go                                                                                                                                                                                                        | Next                                                                                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://github.com/OvidijusParsiunas/deep-chat/tree/main/example-servers/node/express" target="_blank"><img src="./website/static/img/expressLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> | <a href="https://github.com/OvidijusParsiunas/deep-chat/tree/main/example-servers/node/nestjs" target="_blank"><img src="./website/static/img/nestLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> | <a href="https://github.com/OvidijusParsiunas/deep-chat/tree/main/example-servers/python/flask" target="_blank"><img src="./website/static/img/flaskLogo.png" width="60" style="display: block; margin: 0 auto;"/></a> | <a href="https://github.com/OvidijusParsiunas/deep-chat/tree/main/example-servers/java/springboot" target="_blank"><img src="./website/static/img/springBootLogo.png" width="50" style="display: block; margin: 0 auto;"/></a> | <a href="https://github.com/OvidijusParsiunas/deep-chat/tree/main/example-servers/go" target="_blank"><img src="./website/static/img/goLogo.png" width="40" style="display: block; margin: 0 auto;"/></a> | <a href="https://github.com/OvidijusParsiunas/deep-chat/tree/main/example-servers/nextjs" target="_blank"><img src="./website/static/img/nextLogo.png" width="55" style="display: block; margin: 0 auto;"/></a> |

## :construction_worker: Local setup

```
# Install node dependencies:
$ npm install

# Build the component:
$ npm run build

# Automatically build the component as soon as you make a change:
$ npm run build:watch

# Serve the component locally (from index.html):
$ npm run serve

# Bundle the component into a single file (dist/activeTable.bundle.js):
$ npm run build:bundle
```

## :heart: Contributions

Open source is built by the community for the community. All contributions to this project are welcome!<br>
Additionally, if you have any suggestions for enhancements, ideas on how to take the project further or have discovered a bug, do not hesitate to create a new issue ticket and we will look into it as soon as possible!