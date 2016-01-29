# Data object
Bootstrap extras ("BSX") will ship with a standard data model -including Model and Collection constructors. The Data object will be used, primarily, by the Table component for client side pagination, sorting and filtering.

___Note___: _If you are using Bankbone, BSX will opt to use the Model and Collection constructors from the Bankbone library._

## Model

`Model.extend(properties, [classProperties])`

`Model.initialize()`

`Model.cid`

`Model.defaults`

`Model.escape(attribute)` 

## Collection

`Collection.extend(properties, [classProperties])`

`Collection.comparator`

`Collection.length`

`Collection.sort([options])`

`collection.filter(options)`

`collection.paginate(options)`
