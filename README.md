# cncjs-widget-boilerplate [![build status](https://travis-ci.org/cncjs/cncjs-widget-boilerplate.svg?branch=master)](https://travis-ci.org/cncjs/cncjs-widget-boilerplate) [![Coverage Status](https://coveralls.io/repos/github/cncjs/cncjs-widget-boilerplate/badge.svg?branch=master)](https://coveralls.io/github/cncjs/cncjs-widget-boilerplate?branch=master)

### Creating Custom Widgets for CNCjs

You can download a working example widget from the releases page:<br>
https://github.com/cncjs/cncjs-widget-boilerplate/releases

![image](https://user-images.githubusercontent.com/447801/30728860-bbccd270-9f8d-11e7-90e2-7777651bbb59.png)

## Installation

```bash
npm i -g npm # Upgrade NPM to the latest version
npm install
```

## Development

Run `npm run dev` to start a local development server for development, then connect to http://localhost:5000 and wait until bundle finished.

You can specify a mount path to test your widgets with CNCjs:
```bash
cnc -vv --mount /widget:/path/to/cncjs-widget-boilerplate/dist
```

## Production

Run `npm run prepublish` to build production code. It will output index.html, fonts, images, and JavaScript files to the dist folder. 

After that, you can copy all dist files to a directory (e.g. /home/widget), and specify a mount path for the static directory, as shown below:
```bash
mkdir -p /home/widget
cp -af /path/to/cncjs-widget-boilerplate/dist/* /home/widget
cnc --mount /widget:/home/widget
```

## License

MIT
