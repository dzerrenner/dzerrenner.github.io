---
layout: post
title: Using Chrome Logger with Flask
---

A few months ago, i was fiddling around with [Flask](http://flask.pocoo.org/). For some reason, I wanted to log some info from the server side code into the browser. I looked around and discovered [Chrome Logger](http://craig.is/writing/chrome-logger), which is capable to do exactly that. 

Chrome Logger is a Chrome extension which evaluates specific headers sent from a web application to the browser and displays the extracted data in the console of the developer tools. It is backed by server side scripts available for different programming languages. For Python, there is [chromelogger-python](https://github.com/ccampbell/chromelogger-python).

Using this with Flask is quite simple, here is my contribution to the repo (pull-request is still pending, i guess, that it is not really maintained):

```python
# put this somewhere in your application setup

if app.debug:
    import chromelogger as console
 
    @app.after_request
    def chromelogger(response):
        header = console.get_header()
        if header is not None:
            response.headers.add(*header)
        return response
```

The additional headers will only be inserted if debug is activated. This allows yout to leave the `@app.after-request`-handler in your production code without being executed.