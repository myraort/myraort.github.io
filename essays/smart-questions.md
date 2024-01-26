---
layout: essay
type: essay
title: "Smart and Dumb Questions??"
# All dates must be YYYY-MM-DD format!
date: 2024-01-25
published: true
labels:
  - Questions
  - Answers
  - Stack Overflow
---

<img width="175px" 
     class="rounded float-start pe-4" 
     src="../img/smart/smart.jpeg" >

Throughout my school life, I’ve had teachers emphasize that “There are no such things as stupid questions,” highlighting the value of not being afraid of inquiry in learning. Although this may be true when we’re younger, but as we grow into more mature and mindful adults, it is not the case.  In the essay ["How To Ask Questions The Smart Way,"](http://www.catb.org/esr/faqs/smart-questions.html) by Eric Raymond, offers guidance on being an effective communicator when posting questions in forms. I do believe that critically thinking and asking a good question is an essential skill in life despite whatever job you’re in.

## SWE Loves Smart Questions! ##

Since software engineers usually work in a collaborative and fast-paced environment, asking smart questions is crucial. It’s a critical skill that leads to efficient problem solving, clear communication, and community contribution. The ability to ask smart questions enhances teamwork and helps clarify any potential issues along the way. 

## So, What Makes A Question Smart? ## 

A smart question must have a clear purpose or goal with a certain objective in mind. It should demonstrate that the person who is asking the question made a genuine effort to solve the problem before asking for help. Such as, looking it up on the internet, troubleshooting, and reading documentation. Smart questions also consider the time and effort of the reader and make sure that they are not wasting their time as well. 


Stack Overflow is a valuable question and answer platform for programmers that serves as a great tool for those seeking assistance with coding issues or to broaden their coding skills and knowledge. Let’s look at some examples:

```
I've got an ApolloServer project that's giving me trouble, so I thought I might update it and ran into issues when using the latest Babel. My "index.js" is:

require('dotenv').config()
import {startServer} from './server'
startServer() 
And when I run it I get the error

SyntaxError: Cannot use import statement outside a module

First I tried doing things to convince TPTB* that this was a module (with no success). So I changed the "import" to a "require" and this worked.

But now I have about two dozen "imports" in other files giving me the same error.

*I'm sure the root of my problem is that I'm not even sure what's complaining about the issue. I sort of assumed it was Babel 7 (since I'm coming from Babel 6 and I had to change the presets) but I'm not 100% sure.

Most of what I've found for solutions don't seem to apply to straight Node. Like this one here:

ES6 module Import giving "Uncaught SyntaxError: Unexpected identifier"

Says it was resolved by adding "type=module" but this would typically go in the HTML, of which I have none. I've also tried using my project's old presets:

"presets": ["es2015", "stage-2"],
"plugins": [] 
But that gets me another error: "Error: Plugin/Preset files are not allowed to export objects, only functions."

Here are the dependencies I started with:

"dependencies": {
  "@babel/polyfill": "^7.6.0",
  "apollo-link-error": "^1.1.12",
  "apollo-link-http": "^1.5.16",
  "apollo-server": "^2.9.6",
  "babel-preset-es2015": "^6.24.1", 
```

This [question](https://stackoverflow.com/questions/58384179/syntaxerror-cannot-use-import-statement-outside-a-module)  on Stack Overflow meets the criteria of a smart question. The user is running an ApolloServer project but they keep getting this error, “SyntaxError: Cannot use import statement outside a module.” (Add code) The question was very informative and the user provided examples on how they tried to troubleshoot the error and explained what the root of the problem was. The user received multiple answers that answered the main question. The answers were clear, informative, and free of sarcasm and hostility of “hackers.”

## The Opposite ##

While there are a decent amount of questions on Stack Overflow, there are a lot of questions that could use some improvement.

In this [question](https://stackoverflow.com/questions/77882453/how-do-i-create-a-chat-widget-embed-script) the user is asking how to create an embedded chat widget. 

```
I built a chat application(React) similar to ChatBot.com(LiveChat) and I am trying to create an embed script that people could include on their site.

Live example: you can see right side bottom corner chat widget. https://www.chatbot.com/integrations/livechat/

Please how do I achieve this. Thanks.

```

As you can see, the user provides minimal information on what he is trying to look for. The user gave an example of a site with his potential outcome but did not provide any detail of their own project. The user should have done more research on their potential project and could’ve asked a more specific and detailed question for the reader.

## Conclusion ##

The ability to ask smart questions is not just about obtaining answers. It’s about asking in a way that helps everyone; for both the user and readers. This improves the entire community by fostering clear and helpful conversations. Good questions lead to better understanding and teamwork for everyone involved. So, next time you have a question, think to yourself: is it a smart one?

Used ChatGPT for grammar checks and spelling errors.

