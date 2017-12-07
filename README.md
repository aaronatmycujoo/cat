# 🐱

A very simple React and JSX ready webpack config with hot reloading and all that babel goodness 😍

## Prerequisites

- node ^6
- yarn (install it through `npm i yarn -g`)

## Setting up

```
git clone https://github.com/aaronatmycujoo/cat.git
cd cat
yarn
npm run dev
chrome http://localhost:8080
atom . # or `nano app/app.js` amirite
```

Now edit away! 🎉

## Building

```
npm run build
```

Upload the `./public/` anywhere and serve `index.html`.

## Running the app in production mode

```
npm run start
```

It will build the application, then start an express server on some port (probably `6201`), whilst serving the `./public/` folder which the built should be in.

## Analysing

`npm run analysis`

It will build the production application, analyse it, and open the results in a browser. This graph will help you:

- Clearly see what's really inside the application
- Find out what modules make up the most of it's size
- Find modules that got there by mistake

## Meta

### What's the `vendor.js` file that is being built?

This (at the time of writing) includes `react` and `react-dom`. The idea is that it splits up your application into two bundles: your code, and the libraries/modules that you used. Respectively, that is one that changes often, and one that do not change often. It helps with caching so if you were to deploy a small change to your application code and not update a library, then the client can keep it's cached vendor bundle.

It is defined in `entry.vendor` inside `config/webpack.config.prod.js`.
