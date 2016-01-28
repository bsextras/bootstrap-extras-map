# Third-party technology
Bootstrap extras ("BSX") leverages third-party libraries for collaboration, rapid development, documentation and distribution. The scope of this document is to explain which third-party resources are used, and how they are being incorporated.

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
BSX's functionality will depend on the following libraries being present at run-time.

### jQuery
[jQuery][1] (version 1.9.1 or greater) is a direct dependency of both _Bootstrap's_ JavaScript components & BSX. Similar to Bootstrap, each JavaScript component will be exposed as a jQuery plugin.

```javascript
$('#table').table();
```

In addition to using jQuery as a mode of delivery, BSX will utilize jQuery's [Ajax][2] and [Event][3] apis.

___Note___: _Although the components are jQuery plugins, in most cases DOM manipulation will be handled in native JavaScript for performance reasons (see [Code guidlines][4] for more information)._

### Bootstrap
Being that BSX is an extension library of [Bootstrap][5], both Bootstrap's CSS and JS files are direct dependencies. BSX will leverage and build upon the fantastic CSS library developed by Bootstrap, as well use JavaScript to bring the components to life. BSX will employ the lazy-loading concept used by Bootstrap.

```html
<table data-toggle="table">
  ...
</table>
```

___Note___: _BSX is compatible with Bootstrap versions 2 & 3. At the time of development, Bootstrap 4 is in it's infancy stage -barring any fundamental changes in the framework, we anticipate BSX being compatible with version 4 as well. In the event of non-compatibility, we will reserve BSX v2 for being Bootstrap 4 compatibility._

## Drop-in libraries
The following libraries are __not__ dependencies of BSX. However, they will be utilized (by the [Helper][6] & [Data Object][7]) if already present. We made these libraries optional to limit the number or dependencies and to keep BSX as lightweight as possible -as the vast majority of these libraries would not be utilized. The reason we inherit functionality from them (aside from just being awesome libraries), is that the Helper and Data Object will not likely be maintained as frequently.

_Although the functional approach may change, we will ensure that the interfaces of these libraries remain identical._

### Underscore
The Helper library will inherit any intersecting methods from [Underscore][8] (if present). The Helper library is not a constructor, so we will not inherit underscore's chaining functionality. For more information and a list of which methods would be inherited, see [Helper: Intersecting methods][9].

### Backbone
The Data Object library will inherit the Model & Collection constructors from [Backbone][10] (if present). The Data Object library is an even more, bare-bones version Backbone with only functionality specific to the Table component. For more information see [Data Object][7].


## Development dependencies

### Sass
BSX uses [Sass][11] (Syntactically Awesome StyleSheets) to pre-process our CSS files. All CSS, used by BSX, will be firstly written in Sass, then compiled to CSS, then minified.

### Grunt
BSX uses the [Grunt][12] (~0.4.5) task runner for minification, compilation, unit testing and linting.

#### Grunt plugins
- grunt-autoprefixer (~3.0.3)
- grunt-contrib-clean (~0.7.0)
- grunt-contrib-concat (~0.5.1)
- grunt-contrib-copy (~0.8.1)
- grunt-contrib-cssmin (~0.14.0)
- grunt-contrib-uglify (~0.11.0)
- grunt-contrib-watch (~0.6.1)
- grunt-csscomb (~3.1.0)
- grunt-sass (^1.0.0)
- grunt-scss-lint (^0.3.8)

## Documentation

### JSDoc

### Jekyll

### GitHub Pages


[1]: https://jquery.com/ "jQuery"
[2]: https://api.jquery.com/jQuery.ajax/ "jQuery Ajax"
[3]: https://api.jquery.com/category/events/ "jQuery Events"
[4]: https://github.com/bsextras/bootstrap-extras-map/blob/master/code-guidelines/ "Code guidelines"
[5]: http://getbootstrap.com/ "Bootstrap"
[6]: https://github.com/bsextras/bootstrap-extras-map/blob/master/helper/ "Helper"
[7]: https://github.com/bsextras/bootstrap-extras-map/blob/master/helper/data-object "Data object"
[8]: http://underscorejs.org/ "Underscore"
[9]: https://github.com/bsextras/bootstrap-extras-map/blob/master/helper/ "Helper: Intersecting methods"
[10]: http://backbonejs.org/ "Backbone"
[11]: http://sass-lang.com/ "Sass: Syntactically Awesome StyleSheets"
[12]: http://gruntjs.com/ "Grunt: Task runner"
