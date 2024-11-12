# xAI Chat

A simple chat interface for xAI's API.

![demo](./demo.gif)

## Usage

1. Go to [kakkoidev.github.io/xai-chat](https://kakkoidev.github.io/xai-chat)
2. Enter your xAI API key in the prompt
3. Start chatting

If you don't have an API key, you can get one from the [xAI console](https://console.x.ai/).

If you would like to user a different API key, you can do so by clicking the Options > UPDATE API KEY button.

⚠️ The API key and the chat history are stored in your browser's local storage.

## Features

- Markdown support: Messages are rendered as markdown.
- Auto-save: The chat is auto-saved to local storage, so you can come back to it later.
- Auto-scroll to bottom: The chat will automatically scroll to the bottom when a new message is received.
- Clear chat: The chat can be cleared by clicking the CLEAR CHAT button.
- Update system message: The system message (the message that is sent to the API to set the behavior of the chat) can be updated by clicking the UPDATE SYSTEM MESSAGE button.
- Update API key: The API key can be updated by clicking the UPDATE API KEY button.
- Toggle streaming: The streaming (the feature that allows the chat to be streamed in real-time) can be toggled by clicking the STREAMING button.
- Change temperature: Make the output more or less random by changing the temperature. 0 is the most deterministic, 2 is the most random.
- Change max tokens: Change the maximum number of tokens in the response.
- Change frequency penalty: Number between -2.0 and 2.0. Positive values penalize new tokens based on their existing frequency in the text so far, decreasing the model's likelihood to repeat the same line verbatim.
- Change presence penalty: Number between -2.0 and 2.0. Positive values penalize new tokens that are similar to tokens earlier in the text, decreasing the model's likelihood to repeat the same line verbatim.
- Change top p: An alternative to sampling with temperature, called nucleus sampling, where the model considers the results of the tokens with top_p probability mass. So 0.1 means only the tokens comprising the top 10% probability mass are considered. It is generally recommended to alter this or `temperature` but not both.
- Show tokens: Show the number of tokens in each message.
- Show cost: Show the cost of each message.

## Todo

- [ ] Add a button to copy the chat history to clipboard
- [ ] Add a button to download the chat history as a markdown file
- [ ] Add a button to upload a markdown file to continue the chat
- [ ] Abort request
- [ ] Use marked to format user and system messages (make new line with only 1 `\n`)
- [ ] make input a div with `contenteditable` attribute with [Ctrl+Shift] to create a new line
- [ ] add simple project bundler
- [x] show token usage
- [ ] refactor `x-date`
- [ ] add demo gif for each feature
- [ ] add a stack section
- [ ] add resources section

