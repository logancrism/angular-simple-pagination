# Angular Simple Pagination

---
[![GitHub tag](https://img.shields.io/github/tag/raoulus/angular-simple-pagination.svg)]()
[![GitHub tag](https://img.shields.io/github/license/raoulus/angular-simple-pagination.svg)]()

## About
Simple pagination directive for AngularJS. It's tested against angular 1.4.8.

## Installation
```
npm install angular-simple-pagination
```

## Usage
Module:
```javascript
angular.module('YOUR_MODULE', ['angularSimplePagination']);
```

Controller:
```javascript
angular.module('YOUR_MODULE').controller(function($scope) {
  $scope.settings = {
    offset: 0,
    pageLimit: 5,
    pageLimits: ['10', '50', '100']
  };

  $scope.items = [...];
});
```

HTML:
```html
<simple-pagination
  offset="settings.offset"
  page-limit="settings.pageLimit"
  page-limits="settings.pageLimits"
  total="items.length">
</simple-pagination>

<div ng-repeat="item in (items | limitTo:settings.pageLimit:settings.offset)">
...
</div>
```

## Demos
1. [Simple example](http://raoulus.github.io/angular-simple-pagination/)

## Tasks
```bash
gulp build
gulp test
```
