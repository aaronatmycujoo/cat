# 🐱

A very simple React and JSX ready webpack config with hot reloading and all that babel goodness 😍

### Prerequisites

- node ^6

### Setting up

```
git clone https://github.com/aaronatmycujoo/cat.git
cd cat
yarn
npm run dev
chrome http://localhost:8080
atom . # or `nano app/app.js` amirite
```

Now edit away! 🎉

### Building

```
npm run build
```

Upload the `./public/` anywhere and serve `index.html`.

### Express server

#### Prerequisites

- Building

If you want to host it locally after it's been built and see what it's like, run

```
npm run start
```

It will start an express server on some port (probably `6201`) whilst serving the `./public/` folder which the built should be in.
