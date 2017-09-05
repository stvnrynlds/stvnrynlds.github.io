---
layout: post
title:  "Beginning with React"
date:   2017-09-04 9:00:00 -0700
categories: dev, workflow
---

> the grass ain't always greener on the other side / 
> it's green where you water it

The Javascript scene is a [confusing](https://hackernoon.com/how-it-feels-to-learn-javascript-in-2016-d3a717dd577f) and [rapidly expanding](https://trends.google.com/trends/explore?date=all&q=javascript%20frameworks) place. In the past I've made the mistake of thinking that reading equals proficiency. It doesn't. Reading critiques of frameworks I've never used is dangerous, because it only makes me feel smarter. Until I build something, that knowledge is dead weight. 

The key is to build, build, build. Only then are those articles safe to read (and even then in very small doses.)

## Choose Quickly, then Wisely

But how do you choose your tools? If you're a seasoned developer, sustained reflection might be helpful. But if you're just building up your courage to jump, here's my advice: jump. Quickly weigh the options and then make your best guess. Pick something and wrestle with it until you know enough to decide if it's what you want or if you need to jump ship.

I chose [React](https://facebook.github.io/react/). I liked what I saw and it made sense to me, so I chose it. Maybe you wouldn't, maybe you didn't. If so, feel free to read someone else's blog, and best of luck.

For the rest of us, enough prologue. Let's code.

## Installing Node.JS

Assuming you have your [development environment set up](/blog/the-setup/), we're going to head to the terminal to install [NodeJS, the JavaScript runtime](https://www.reddit.com/r/learnjavascript/comments/3d4hs5/eli5_what_in_the_heck_is_nodejs/) we'll be using to develop our React app.

0. Install NVM ([Node Version Manager](https://github.com/creationix/nvm)) via the command line: 
``` sh
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.3/install.sh | bash
```
(You may need to restart your terminal after this step.)

0. Install [Node](https://nodejs.org/en/):
```
nvm install node
```
0. Check your Node version:
```
nvm version
```
You should see `v8.4.0` or higher. Success!

Included with Node is a command-line interface called NPM ([Node Package Manager](https://www.npmjs.com/)). This is like `brew` for Macs, or `apt` for Linux: it handles installing, removing, and updating bundles of code called packages. You'll use it frequently in React.

## Using Create React App
In order to get us up and running, I'm going to be using a tool called [Create React App](https://github.com/facebookincubator/create-react-app) which sets us up with the best practices for a new React app. In a future post I'll show what's going on under the hood by ejecting from Create React App and looking at its packages, but for now let's move forward:

0. Install Create React App via NPM:
```
npm install -g create-react-app
```
The `-g` flag in this command stands for `--global`, which means that Create React App can be run anywhere, not just in a particular directory. You may also see `install` shortened to `i`, like so: `npm i -g create-react-app`.
0. Create a new project (I'm calling this one `my-app`):
```
create-react-app my-app
```
You should immediately see the following response with a progress bar below it:
```
Creating a new React app in /Users/You/my-app.
Installing packages. This might take a couple of minutes.
Installing react, react-dom, and react-scripts...
```
0. Once it finishes, you should see a success message. `cd` into your project directory and start the app:
```
cd my-app
npm start
```
0. Soon after entering `npm start`, you should see a message notifying you that your app is running locally:
```
You can now view my-app in the browser.
Local:            http://localhost:3000/
```
If you wish to kill the server at any point, just hit `ctrl + C` in the terminal. You can just `npm start` it back up!

0. Open Chrome and go to `http://localhost:3000/` (or whichever URL it provides you). If you see a "Welcome to React" page, congrats! You did it. Your very first React app.

Before we move on, let's leave our mark. The React Welcome page says:
> "To get started, edit src/App.js and save to reload."

Let's do just that. Open `my-app` in your text editor, and locate `src/App.js`. 

Make a change, like updating the messsage to `<h2>Hello World!</h2>`, and hit save. Notice that the page gets hot reloaded, no refresh necessary.

## Using React Dev Tools
One last piece of this puzzle, you'll want to install [Chrome's React Developer tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi). They'll let you inspect your app's structure, props, and state, which the typical Dev Tools can't do. 

0. Go to the Chrome Store and find [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi). Click "Add to Chrome".
0. Once it installs, you'll see a grayed-out icon in the upper right corner of the browser.
0. Go back to your new app, and you'll see that grayed-out icon become colorized once it detects a React App on the page. 
0. Open Chrome's Dev Tools (⌘ + ⌥ + I). There should be a new tab named "React". Now you can easily inspect your app.

## Next Week

Stay tuned as we investigate components, the building blocks of a React app.