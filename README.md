Australian Business Number (ABN) directive [![Build Status](https://api.travis-ci.org/JMontagu/ng-AustralianBusinessNumber.png)](https://travis-ci.org/JMontagu/ng-AustralianBusinessNumber)
==========
ABN validation directive for AngularJS. Uses the Australian Taxation Office (ATO) [ABN verification formula](http://www.ato.gov.au/Business/Australian-business-number/In-detail/Introduction/Format-of-the-ABN/).

# Demo
View the demo at [jmontagu.github.io/ng-AustralianBusinessNumber/](http://jmontagu.github.io/ng-AustralianBusinessNumber/)

# Usage
1. Add [src/australianBusinessNumber.js](https://github.com/JMontagu/ng-AustralianBusinessNumber/blob/master/src/australianBusinessNumber.js) to your solution
2. Add the australianBusinessNumber module as a dependency to your application module:

    ```javascript
    var myAppModule = angular.module('MyApp', ['australianBusinessNumber']);
    ```
3. Add the attribute 'abn' to your form elements like so:

    ```html
    <input abn type="text" ng-model="client.abn" />
    ```

To make the element mandatory:

```html
<input abn required type="text" ng-model="client.abn" />
```

To display a validation error:

```html
<form name="form">
	<input name="abnInput" ng-model="client.abn" abn />
	<span ng-show="form.$error.abnInput">Invalid ABN</span>
</form>
```


# Requirements
- [AngularJS](http://angularjs.org/)

## Project setup
1. Install **Karma**, **Grunt**, **Bower**
  `$ npm install -g karma grunt-cli bower`
2. Install development dependencies
  `$ npm install`
3. Install components
  `$ bower install`

## Testing
This project uses [Grunt](http://gruntjs.com/) to check for JavaScript syntax errors and execute all unit tests. To run Grunt, simply execute:

`$ grunt`

# License
This code is released under the MIT license. 
