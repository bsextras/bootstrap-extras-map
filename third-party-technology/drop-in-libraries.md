# Drop-in libraries
The following libraries are __not__ dependencies of BSX. However, they will be utilized (by the [Helper][1] & [Data Object][2]) if already present. We made these libraries optional to limit the number or dependencies and to keep BSX as lightweight as possible -as the vast majority of these libraries would not be utilized. The reason we inherit functionality from them (aside from just being awesome libraries), is that the Helper and Data Object will not likely be maintained as frequently.

_Although the functional approach may change, we will ensure that the interfaces of these libraries remain identical._

## Underscore
The Helper library will inherit any intersecting methods from [Underscore][3] (if present). The Helper library is not a constructor, so we will not inherit underscore's chaining functionality. For more information and a list of which methods would be inherited, see [Helper: Intersecting methods][4].

## Backbone
The Data Object library will inherit the Model & Collection constructors from [Backbone][5] (if present). The Data Object library is an even more, bare-bones version Backbone with only functionality specific to the Table component. For more information see [Data Object][2].

[1]: https://github.com/bsextras/bootstrap-extras-map/blob/master/helper/ "Helper"
[2]: https://github.com/bsextras/bootstrap-extras-map/blob/master/helper/data-object "Data object"
[3]: http://underscorejs.org/ "Underscore"
[4]: https://github.com/bsextras/bootstrap-extras-map/blob/master/helper/ "Helper: Intersecting methods"
[5]: http://backbonejs.org/ "Backbone"
