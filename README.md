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

## How Does It Work?

- What is a system prompt? A system prompt is a message sent to the API to set the behavior of the chat.
- What is a user? A user is the person sending messages to the chat.
- What is an assistant? An assistant is the AI answering the messages.
- What is a token? A token is the smallest unit of text that can be processed by the API.
- How are costs calculated? The cost is calculated based on the number of tokens in the input (what you write to the chat) and output (what the AI writes to the chat).
- What is streaming? Streaming is the feature that allows the chat to be streamed in real-time.
- What is temperature? Temperature is a parameter that controls the randomness of the AI's output. 0 is the most deterministic, 2 is the most random.

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
- Chat input: You can send messages to the AI by typing in the chat input area and pressing `Enter`. If you press `Shift+Enter`, a new line will be created without sending the message.

## Stack

- HTML
- CSS
- [Alpine.js](https://alpinejs.dev/)
- [marked](https://marked.js.org/) to render markdown
- [x.ai API](https://x.ai/api)
- [GitHub Pages](https://pages.github.com/) to host the application

## Reflections

- The AI is not your friend. It is a soulless machine.
- Always double check the AI's answer.
- I learned about the xAI API from this Youtube video: https://www.youtube.com/watch?v=Tw696JVSxJQ
- The minimalistic design of this app is inspired by [Universal Paperclip](https://www.decisionproblem.com/paperclips/).
- The symbol for the token counter ₮ is actually the symbol for the [Mongolian tugrik (the currency of Mongolia)](https://en.wikipedia.org/wiki/Tugrik). I found it by looking for symbols looking like a T for the token counter. It was listed as crypto currency character on [unicode-explorer.com](https://unicode-explorer.com/articles/cryptocurrency-unicode-symbols), apparently it is also used by a cryptocurrency called Tether.
- Pricing wise, xAI is about the price of Anthropic's Claude Sonnet 3.5. 3x more expensive than OpenAI's GPT-4o. 3x cheaper that Anthropic's Claude 3.1. Take it into account when choosing the right tool for your needs.
- To limit cost, I advice you to start new conversations regularly. Ask the AI to summarize the conversation or copy the code snippet you are working on, clear the chat, and start a new conversation.
- The AI won't "do the code for you" - it is often wrong in its assumptions- approach to the problem and needs to be "cohearsed" into giving you the right answer. Understanding what you are doing is essential and thinking at a higher level of abstraction will yield better results. The AI output a lot of content but the finer thinking depends on you.
- If you have a network error, just try again by prompting the AI with the word "again" or "retry".
- The default parameters are great for software engineering (concise and repeatable, deterministic) -- maybe playing with the parameters would be advised to get something for creative (poetry...) or more human-like (chat app, psychological help, debate...).
- I'm starting to think that the system prompt is very important in the quality of the output (hidden in commercial apps, interesting topic to explore!).

## Ideas

- Add speech-to-text and text-to-speech AI features.
- Add an image recognition feature.
- Add an image generation feature.
- Make it a desktop app.
- Run self-hosted AI models.
- Fine-tune models.
- Train new models.

## Known bugs

- On mobile, scrolling up doesn't stop the auto-scroll. Just turn off auto-scroll in the options.

## Todo

- [ ] Abort request
- [x] Use marked to format user and system messages (make new line with only 1 `\n`)
- [x] make input a div with `contenteditable` attribute with [Ctrl+Shift] to create a new line
- [ ] add simple project bundler
- [x] show token usage
- [ ] refactor `x-data`
- [ ] add demo gif for each feature
- [x] add a stack section
- [ ] add resources section
- [x] handle fetch error
- [ ] when changing the value of a slider, the value should be updated immediately
- [ ] add auto-scroll toggle button
- [ ] add a conversations menu to select a conversation to load, conversation menu displays as a sidebar and can edit tile and delete conversations
- [x] add reflections section in readme 
- [ ] add images and gifs in the reflections section
- [x] add ideas section in readme
- [x] Known bugs section in readme
- [ ] add a "notes" sidebar that opens on the side of the chat
- [ ] rename "options" to "menu" and organize it in sections: Setup, Tools, Options, Info
- [ ] auto-save the input text
- [ ] remove text formatting in the input area
- [ ] add a button to get human help! It will automatically prepare a message to ask help summarizing the conversation in order to post it on a forum, a chat, etc.
- [ ] add history of all api calls, with date, tokens, cost, status, feature of the app that made the call...
- [x] add section in readme "How does it work?"

