+++
date = "2016-02-15T09:40:58-06:00"
draft = true
title = "Using Trello's REST Authentication Token"
tags = ["til", "trello", "rest"]
categories = ["til", "trello"]
+++

Trello has a pretty useful REST API that you can use to interact with your
Boards and such.  In using Trello, the documentation seems to focus on using
a `client.js` file, where I am simply want to call Trello with an API key or
some other credential.  Well, after scouring the internet, it seems there are
some options that make this possible / easier.

Get your Trello API APP key and Secret from here: https://trello.com/app-key

## Generate a Token

Using the App Key and Secret, you can generate a Token (expirable if you wish)
that you can use for future calls.  I mention that they recommend the
`client.js` file, but if you want, take a look at it.  It basically generates
a URL https://trello.com/1/connect?key=...&name=MyApp&response_type=token or
https://trello.com/1/connect?key=...&name=MyApp&response_type=token&scope=read,write
depending on your scope that you'd like.  You can also pass in an `expiration`
and some other options.  Many of these are explained in the documentation for
[`client.js`](https://developers.trello.com/clientjs).

