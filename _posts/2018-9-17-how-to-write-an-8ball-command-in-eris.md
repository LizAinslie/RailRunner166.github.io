---
layout: post
title: "How to Write an 8ball Command in Eris"
summary: Today we will write an 8-ball command for a Discord bot in Eris.
featured-img: pau-casals-588027
categories: [Guides, Discord]
---

8-Ball is one of the most basic Discord bot commands, making it a staple in most all bots. I have one that I wrote a long time ago, and today I want to share it with you.

The first thing you will need is an array of responses. Put it outside of your run function.
```js
const responses = [
    // Responses go here...
]
// Run function below this line
```

Some common responses for 8-ball commands are:

- It is certain
- It is decidedly so
- Without a doubt
- Yes, definetly
- You may rely on it
- As I see it, yes
- Most likely
- Outlook good
- Yes
- Signs point to yes
- Reply hazy try again
- Ask again later
- Better not tell you now
- Cannot predict now
- Concentrate and ask again
- Don't count on it
- My reply is no
- My sources say no
- Outlook not so good
- Very doubtful

Since I used to use Discord.js, my run function goes as follows:

```js
// responses array above this line
exports.run = (client, message, args) => {
    // Command code
}
```

The code that goes inside the run function starts with this line:

```js
if (args.length < 1) return message.channel.createMessage(':question: │ Missing `&lt;question&gt;` option.')
```

Lets digest this line. It checks to see if there are no arguments, and if there are none, it replies with: ``Missing `<question>` option.``

The next line goes as follows:
```js
if (!(args[args.length - 1].endsWith('?'))) return message.channel.createMessage('Missing a `?`.')
```

You can choose whether you want to include this line or not, all it does is check whether there is a `?` or not at the end of the message, and rejects it if not.

The last line is what determines the 8-ball response and sends it to the user.
```js
message.channel.createMessage(responses[Math.floor(Math.random() * responses.length)])
```

This sends a random response from the responses array to the user.

The final code for this tutorial can be found [On Github](https://gist.github.com/RailRunner16/fe254169d826a2ccebeabba1924acb56).