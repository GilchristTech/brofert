# Brofert: Browser Feature Report

Sometimes, it can be helpful to get a bunch of browser
information. Occasionally, one has a website which is displaying
weirdly on someone else's browser, and needs some details.
Browser Feature Report, or Brofert for short, is designed for
this purpose.

Brofert collects data on browser features into an HTML table
format on page load, and a JSON structure for sending the report
elsewhere.

## Building and Serving

Currently, Browser Feature Report has no build process!
Everything is contained within a single static HTML file. You
could say it's a Single-Page Application. Copy `index.html`
wherever you want.

However, this repo provides a Node package for running a server
with NPM, for convenience:

```bash
npm i
npm start
```

You can also run a server with various quick HTTP server
programs:

```bash
python -m http.server
npx http-server
```

## Backwards Compatibility

Brofert has been tested in Linux Chrome and Firefox, but also
the Kindle web browser, Internet Explorer 6, Internet
Explorer 5, and Netscape Navigator 6. 

The idea is that if it works on something like IE5, it'll work on
anything.

Notably, IE5 was the Internet Explorer version with JScript 5.0,
which introduced `try`/`catch`, a feature central to Brofert's
feature detection. If you or your users are on something older
than that, I apologize, it may be time for an update.
