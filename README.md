# xAI Chat

A simple chat interface for [xAI's API](https://x.ai/api).

![demo](./demo.gif)

xAI's Grok chat UI is not yet available in my region, so I made this simple chat interface. It's also the occassion for me to have an hands-on experience with AI chats. To get to know more about how it works, how to tweak it, how to tailor it to my needs, etc.

## Usage

1. Go to [kakkoidev.github.io/xai-chat](https://kakkoidev.github.io/xai-chat)
2. Enter your xAI API key in the prompt
3. Start chatting

If you don't have an API key, you can get one from the [xAI console](https://console.x.ai/).

If you would like to user a different API key, you can do so by clicking the Options > UPDATE API KEY button.

⚠️ The API key and the chat history are stored in your browser's local storage.

## Features

- Single file application with no build step. This is a simple `index.html` file that can be dropped anywhere and "just work". And will still be working in the years to come. Ex: on a CND, ran locally with a static file server...
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

- [ ] Abort request
- [x] Use marked to format user and system messages (make new line with only 1 `\n`)
- [x] make input a div with `contenteditable` attribute with [Ctrl+Shift] to create a new line
- [ ] add simple project bundler
- [x] show token usage
- [ ] refactor `x-data`
- [ ] add demo gif for each feature
- [ ] add a stack section
- [ ] add resources section
- [x] handle fetch error
- [ ] when changing the value of a slider, the value should be updated immediately
- [ ] add auto-scroll toggle button
- [ ] add a conversations menu to select a conversation to load, conversation menu displays as a sidebar and can edit tile and delete conversations
- [ ] add reflections section in readme where talk about pricing, starting new conversations regularly to reduce token carry-over cost (show workflow gif), take the time to understand the AI's answer line by line, expectations (similar to Claude Sonnet 3.5), default parameters are great for software engineering (concise and repeatable, deterministic) -- maybe playing with the parameters would be advised to get something for creative (poetry...) or more human-like (chat app, psychological help, debate...), I'm starting to think that the system prompt is very important in the quality of the output (hidden in commercial apps, interesting topic to explore!), the AI won't "do the code for you" - it is often wrong in its assumptions- approach to the problem and needs to be "cohearsed" into giving you the right answer - understanding what you are is essential and thinking at a higher level of abstraction will yield better results - the AI output a lot of content but the finer thinking depends on you, if you have a network error - just try again by prompting the AI with the word "again" or "retry" lketc.
- [ ] add ideas section in readme: text-to-speech, speech-to-text, image recognition, image generation, desktop app, run local models, fine tune models, train new models, etc.
- [ ] Known bugs section in readme: on mobile scrolling up doesn't stop the auto-scroll (just turn off auto-scroll in the options)
- [ ] add a "notes" sidebar that opens on the side of the chat
- [ ] rename "options" to "menu" and organize it in sections: Setup, Tools, Options, Info
- [ ] auto-save the input text
- [ ] remove text formatting in the input area
- [ ] add a button to get human help! It will automatically prepare a message to ask help summarizing the conversation in order to post it on a forum, a chat, etc.
- [ ] add history of all api calls, with date, tokens, cost, status, feature of the app that made the call...
- [ ] add section in readme "How does it work?": what is a system prompt, a user, an assistant, a token output/input, calculate cost, etc...

