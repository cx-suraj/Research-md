# Using JSReport with more than 5 templates in node server 

## Using JSReport with more than 5 templates in Node server  

In your express app install following packages

```
npm i jsreport-core jsreport-handlebars puppeteer jsreport-chrome-pdf
```

[jsreport-core](https://www.npmjs.com/package/jsreport-core) is the main package and these are the helper package
- `jsreport-handlebars`
- `puppeteer`
- `jsreport-chrome-pdf`

# Implement [jsreport](https://github.com/jsreport/jsreport/tree/master/packages/jsreport-core) in express app

- Create a API entry point in your express app   
```js
app.use('/campaign', campaign);
```
- In your route file import packages
```js
const express = require('express');
const router = express.Router(); 
const jsreport = require('jsreport-core')()
```
- Then import the templates
```js
// In template.js file copy the template files and module.exports it
const { template } = require('./template')
```
- In order to use jsreport we have to intilize it so for that code snippet:
```js
let jsReportInitialized = false;
async function checkIfJsReportIsInit() {
	if (!jsReportInitialized) {
	await jsreport.init();
	jsReportInitialized = true;
	}
	return Promise.resolve();
}
```
- Now create a route
```js
router.get('/printPDF', async function (req, res, next) {});
```
- render a pdf 
	- Inorder to render a pdf  we use `jsreport.render` function
	- it takes a object as a argument
```js
{ 
 "template": { 
	content: template, // here we can provide camapign pdf template
	engine: 'handlebars',
	recipe: 'chrome-pdf',
 }, 
 "data" : { ... }, // here we can provide camapign data
 "options": { "reports": { "save": true } } 
 }
```
- Now let's create a pdf and send it as a response
```js
router.get('/new', async function (req, res, next) {
	try {
		return checkIfJsReportIsInit().then(() => {
			return jsreport.render({
					template: {
					content: template, // giving template
					engine: 'handlebars',
					recipe: 'chrome-pdf'
					},
					data: camapignData, // giving data
				}).then((resp) => {
					resp.stream.pipe(res); // sending generated pdf as a res
				});
			}).catch((e) => {
				console.log("err");
				console.error(e)
			})
	} catch {
			res.send("error")
		}
})
```


