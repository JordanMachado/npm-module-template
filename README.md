# npm-module-template

Template for es6 node module

## Instalation

First time you clone the repository on your computer
```bash
npm install -g init-package-json
```
## Usage

```bash
node init.js
```

## Features

### Create a new README.md with the template bellow

```md
# ${packageName}

${description}

## Instalation
\`\`\`bash
npm install --save ${packageName}
\`\`\`
## Usage

\`\`\`js
const listener = require('${packageName}');
//OR
import listener from '${packageName}'
\`\`\`

#### \`fn\`
description fn
```
### Add automatically in your **package.json**

### babel config
```json
"babel": {
	"presets": [
		[
			"es2015",
			{
				"loose": true
			}
		]
	],
	"plugins": [
		"add-module-exports"
	]
}
```

### babel dependencies & eslint
```json

"devDependencies": {
	"babel-cli": "^6.18.0",
	"babel-plugin-add-module-exports": "0.1.2",
	"babel-preset-es2015": "^6.18.0",
	"babel-preset-es2015-loose": "^8.0.0",
	"babelify": "^7.3.0",
	"eslint": "^3.11.1"
},

```

### scripts for building your library
```json

"scripts": {
	"lib": "babel src --presets=es2015 --plugins=add-module-exports --out-dir lib -s -w",
	"lint": "eslint scripts src test",
	"test": "echo \"Error: no test specified\" && exit 1"
},

```
