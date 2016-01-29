# Helper
Bootstrap extras ("BSX") ships with a helper tool for handling common DOM, object, and array tasks.

## DOM helpers

__addClass__ `_.addClass(elem, className)`
```javascript
var div = document.createElement('div')
_.addClass(div, 'some-class')
```
```html
<div class="some-class"></div>
```

__addClasses__ `_.addClasses(elem, classNames)`
```javascript
var div = document.createElement('div')
_.addClasses(div, ['some-class', 'some-other-class'])
```
```html
<div class="some-class some-other-class"></div>
```

__addClassOnce__ `_.addClassOnce(elem, className)`
```javascript
var div = document.createElement('div')
_.addClass(div, 'some-class')
_.addClassOnce(div, 'some-class')
```
```html
<div class="some-class"></div>
```

__addClassesOnce__ `_.addClassesOnce(elem, classNames)`
```javascript
var div = document.createElement('div')
_.addClass(div, 'some-class')
_.addClassesOnce(div, ['some-class', 'some-other-class'])
```
```html
<div class="some-class some-other-class"></div>
```

__createElement__ `_.createElement(nodeName, [attrs])`
```javascript
var div = _.createElement('div', { id: 'div1' })
```
```html
<div id="div1"></div>
```

__dataAttrs__ `_.dataAttrs(elem)`
```javascript
var div = document.createElement('div')
div.setAttribute('data-key', 'A')
div.setAttribute('data-some-other-key', 'B')
var data = _.dataAttrs(div)
```
```javascript
{ key: 'A', 'someOtherKey': 'B' }
```

__hasClass__ `_.hasClass(elem, className)`
```javascript
var div = document.createElement('div')
_.addClass(div, 'some-class')
_.hasClass(div, 'some-class'      ) >> TRUE
_.hasClass(div, 'some-other-class') >> FALSE
```

__removeClass__ `_.removeClass(elem, className)`

__removeClasses__ `_.removeClasses(elem, classNames)`

## Object helpers

__flattenJson__ `_.flattenJson(object)`: Flattens a JSON object to single level, using dot-notation.
```javascript
var obj = { 'user': { 'id': 1, 'username': 'Joe' } }
_.flattenJson(obj) 
```
```javascript
{ 'user.id': 1, 'user.username': 'Joe' }
```

## Array helpers

__flattenJsonArray__ `_.flattenJsonArray(arr)`: Similar to __flattenJson__, but flattens each item in an array.
```javascript
var arr = [
  { 'user': { 'id': 1, 'username': 'Joe' } },
  { 'user': { 'id': 2, 'username': 'John' } }
]
_.flattenJsonArray(arr) 
```
```javascript
[{ 'user.id': 1, 'user.username': 'Joe' },
 { 'user.id': 2, 'user.username': 'John' }]
```

## Intersecting methods

__filter__ `_.filter(list, predicate, [context])`

__flatten__ `_.flatten(array, [shallow])`

__clone__`_.clone(object)`

__extend__ `_.extend(destination, *sources)`

__extendOwn__ `_.extendOwn(destination, *sources)`

__isEmpty__ `_.isEmpty(object)`

__isElement__ `_.isElement(object)`

__isArray__ `_.isArray(object)`

__isObject__ `_.isObject(object)`

__isFunction__ `_.isFunction(object)`

__isString__ `_.isString(object)`

__isNumber__ `_.isNumber(object)`

__isBoolean__ `_.isBoolean(object)`

__isDate__ `_.isDate(object)`

__isNull__ `_.isNull(object)`

__isUndefined__ `_.isUndefined(object)`

__result__ `_.result(object, property, [defaultValue])`
