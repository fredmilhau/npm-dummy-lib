# npm-dummy-lib

this is a simple template of npm typescript lib

https://codeburst.io/https-chidume-nnamdi-com-npm-module-in-typescript-12b3b22f0724

https://itnext.io/step-by-step-building-and-publishing-an-npm-typescript-package-44fe7164964c

## Installation 
```sh
npm install @fredmilhau/npm-dummy-lib --save
yarn add @fredmilhau/npm-dummy-lib
bower install @fredmilhau/npm-dummy-lib --save
```

## Usage

### Javascript

```javascript
var pluralise = require('mypluralize');
var boys = pluralise.getPlural('Boy');
```
```sh
Output should be 'Boys'
```

### TypeScript
```typescript
import { getPlural } from 'mypluralize';
console.log(getPlural('Goose'))
```
```sh
Output should be 'Geese'
```

### AMD
```javascript
define(function(require,exports,module){
  var pluralise = require('mypluralize');
});
```

## Test 
```sh
npm run test
```