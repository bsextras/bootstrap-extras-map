# Third-party technology
Bootstrap extras ("BSX") leverages third-party libraries for rapid development. The scope of this document is to explain which third-party resources are used, and how they are being incorporated.

## Table of Contents
- [Dependencies](#dependencies)
	- [jQuery](#jquery)
	- [Bootstrap](#bootstrap)
- [Drop-in libraries](#drop-in-libraries)
	- [Underscore](#underscore)
	- [Backbone](#backbone)
- [Development dependencies](#development-dependencies)
	- [Sass](#sass)
	- [Grunt](#grunt)
		- [Grunt plugins](#grunt-plugins)
- [Documentation](#documentation)
	- [JSDoc](#jsdoc)
	- [Jekyll](#jekyll)
	- [GitHub Pages](#github-pages)

## Dependencies

### jQuery
[jQuery][1] (version 1.9.1 or greater) is a direct dependency of both _Bootstrap's JavaScript components_ & _Bootstrap extras_. Similar to Bootstrap, each JavaScript component will be exposed as a jQuery plugin.

```javascript
$('#table').table();
```

___Note___: _Although the components are jQuery plugins, in most cases DOM manipulation will be handled in native JavaScript for performance reasons (see [Code guidlines][2] for more information)._

### Bootstrap
Being that _Bootstrap extras_ is an extension library of [Bootstrap][3], both  the CSS and JS files are direct dependencies. Bootstrap extras will inherit the lazy-loading concept used by Bootstrap.
```html
<table data-toggle="table">
  ...
</table>
```

## Drop-in libraries

### Underscore
[Underscore][4] is __not__ a direct dependency (if you are already using it, Great! -if not, thats great too!). However, the [Helper][5] library will inherit any intersecting methods if underscore is already present. The reason for this separation is to limit the number of dependencies and to keep Bootstrap extras lightweight (as the vast majority of underscore will not be used). The reason we will inherit methods from underscore (aside from being awesome) is that the Helper library will likely not be maintained as frequently.

### Backbone
Like underscore, [Backbone][6] is __not__ a direct dependency. However, the [Data Object][7] library will default to using Backbones' Model and Collection constructors if Backbone is already present. The reason for this separation is to limit the number of dependencies and to keep Bootstrap extras lightweight (as only stripped-down versions of the constructors are used). The reason we default to Backbone (aside from being awesome) is that the Data Object library will likely not be maintained as frequently.


## Development dependencies

### Sass

### Grunt

#### Grunt plugins

## Documentation

### JSDoc

### Jekyll

### GitHub Pages


[1]: https://jquery.com/ "jQuery"
[2]: https://github.com/bsextras/bootstrap-extras-map/blob/master/code-guidelines/ "Code guidelines"
[3]: http://getbootstrap.com/ "Bootstrap"
[4]: http://underscorejs.org/ "Underscore"
[5]: https://github.com/bsextras/bootstrap-extras-map/blob/master/helper/ "Helper"
[6]: http://backbonejs.org/ "Backbone"
[7]: https://github.com/bsextras/bootstrap-extras-map/blob/master/helper/data-object "Data object"
