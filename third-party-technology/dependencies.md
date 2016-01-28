# Dependencies
BSX's functionality will depend on the following libraries being present at run-time.

## jQuery
[jQuery][1] (version 1.9.1 or greater) is a direct dependency of both _Bootstrap's_ JavaScript components & BSX. Similar to Bootstrap, each JavaScript component will be exposed as a jQuery plugin.

```javascript
$('#table').table();
```

In addition to using jQuery as a mode of delivery, BSX will utilize jQuery's [Ajax][2] and [Event][3] apis.

___Note___: _Although the components are jQuery plugins, in most cases DOM manipulation will be handled in native JavaScript for performance reasons (see [Code guidlines][4] for more information)._

## Bootstrap
Being that BSX is an extension library of [Bootstrap][5], both Bootstrap's CSS and JS files are direct dependencies. BSX will leverage and build upon the fantastic CSS library developed by Bootstrap, as well use JavaScript to bring the components to life. BSX will employ the lazy-loading concept used by Bootstrap.

```html
<table data-toggle="table">
  ...
</table>
```

___Note___: _BSX is compatible with Bootstrap versions 2 & 3. At the time of development, Bootstrap 4 is in it's infancy stage -barring any fundamental changes in the framework, we anticipate BSX being compatible with version 4 as well. In the event of non-compatibility, we will reserve BSX v2 for Bootstrap 4 compatibility._

[1]: https://jquery.com/ "jQuery"
[2]: https://api.jquery.com/jQuery.ajax/ "jQuery Ajax"
[3]: https://api.jquery.com/category/events/ "jQuery Events"
[4]: https://github.com/bsextras/bootstrap-extras-map/blob/master/code-guidelines/ "Code guidelines"
[5]: http://getbootstrap.com/ "Bootstrap"
