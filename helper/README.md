# Helper
Bootstrap extras ("BSX") ships with a helper tool for handling common DOM, object, and array tasks.

## DOM helpers

__addClass__ `_.addClass(elem, className)`

__addClasses__ `_.addClasses(elem, classNames)`

__addClassOnce__ `_.addClassOnce(elem, className)`

__addClassesOnce__ `_.addClassesOnce(elem, classNames)`

__createElement__ `_.createElement(nodeName, [attrs])`

__dataAttrs__ `_.dataAttrs(elem)`

__hasClass__ `_.hasClass(elem, className)`

__removeClass__ `_.removeClass(elem, className)`

__removeClasses__ `_.removeClasses(elem, classNames)`

## Object helpers

__flattenJson__ `_.flattenJson(object)`: Flattens a JSON object to single level, using dot-notation.
```javascript
var obj = { 'user': { 'id': 1, 'username': 'Joe' } }
_.flattenJson(obj) 
// { 'user.id': 1, 'user.username': 'Joe' }
```

## Array helpers

__flattenJsonArray__ `_.flattenJsonArray(arr)`: Similar to __flattenJson__, but flattens each item in an array.
```javascript
var arr = [
  { 'user': { 'id': 1, 'username': 'Joe' } },
  { 'user': { 'id': 2, 'username': 'John' } }
]
_.flattenJsonArray(arr) 
// [{ 'user.id': 1, 'user.username': 'Joe' },
//  { 'user.id': 2, 'user.username': 'John' }]
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
