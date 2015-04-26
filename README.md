# Bootstrap Form Input Prefix Icons

The **bootstrap-input-prefix** library is a small add-on for Twitter's Bootstrap CSS framework that enables you to add glyphicons (or Font-Awesome icons) into your form input fields. By default, Bootstrap includes the concept of feedback icons for form fields. These are typically used to place an icon on the inside right of a form field to indicate the validation state of the field (i.e. a checkbox for a valid field). This doesn't allow you to place icons on the inside left of the form field, however. Hence the need for **bootstrap-input-prefix**.

## Screenshot Example

![Screenshot of bootstrap-input-prefix in action](https://cloud.githubusercontent.com/assets/167845/7336618/d9ff3f24-ebff-11e4-88b4-cab1c76fa89e.png)

See the `examples/index.html` file for more usage examples.

## Usage

To use, simply load the CSS file in your HTML page *after* the line where you load Bootstrap:

	<link rel="stylesheet" href="/path/to/bootstrap-input-prefix.min.css">

Using the library works almost identically to the feedback icons that come with Bootstrap itself. Simply add a `has-prefix` class to the `form-group` block, and add the `form-control-prefix` class to the glyphicon. You can also use this library with Font-Awesome icons.

	<div class="form-group has-prefix">
		<label class="control-label">Regular Input Field</label>
		<input type="text" class="form-control" placeholder="Search our site...">
		<span class="glyphicon glyphicon-search text-muted form-control-prefix" aria-hidden="true"></span>
	</div>

The library also works with small and large input fields without any additional classes. Simply add the `input-sm` or `input-lg` class to the `<input>` element like you normally would.

You can also use the library with horizontal forms, for example:

	<form class="form-horizontal">
		<div class="form-group has-prefix">
			<label class="control-label col-sm-3">Regular Input Field</label>
			<div class="col-sm-9">
				<input type="text" class="form-control" placeholder="Search our site...">
				<span class="glyphicon glyphicon-search text-muted form-control-prefix" aria-hidden="true"></span>            
			</div>
		</div>
	</form>

Inline forms work too, but to get them right you need to wrap the input field and the icon in a `span` element with the class `prefix-wrapper`:

	<form class="form-inline">
		<div class="form-group has-prefix">
			<label class="control-label">Regular Input Field</label>
			<span class="prefix-wrapper"> 
				<input type="text" class="form-control" placeholder="Search our site...">                
				<span class="glyphicon glyphicon-search text-muted form-control-prefix" aria-hidden="true"></span>
			</span>
		</div>
	</form>

The icons also inherit validation state colors if you add a `has-success`, `has-warning` or `has-error` class to your `form-group` block. For the color to work, ensure you are not overriding the color of the icon using a class like `text-muted` like I am in the exmaples above.

## Using with Feedback Icons

Note that using the prefix icons and feedback icons on the same field at once is not currently supported. If you try to do this, you'll find that one of the icons displays off the vertical center. This will be addressed in a future release.

## Source

The LESS source code for this library is included in the `src` directory. To build, you will need to import the Bootstrap `variables.less` and `mixins.less` files at a minimum or it will fail.

## Compatibility

The library has been tested with Bootstrap version 3.3.1. Older versions are not supported and there are no plans to do so in the future. It should be compatible with the same desktop and mobile browsers that Bootstrap itself is:

* Chrome (latest version on Windows, Mac OS X, Android and iOS)
* Firefox (latest version on Windows, Mac OS X and Android)
* Internet Explorer (version 8 and above, Windows only)
* Opera (latest version on Windows and Mac OS X only)
* Safari (latest version on Mac OS X and iOS only)

Unofficially, the library should work with Chromium and Chrome for Linux, Firefox for Linux and Internet Explorer 7, but these browsers are not officially supported.

## License

bootstrap-input-prefix is released under the MIT license and is copyright 2015 Array Software. Boiled down to smaller chunks, it can be described with the following conditions.

#### It requires you to:
* Keep the license and copyright notice included in bootstrap-input-prefix's CSS files when you use them in your works

#### It permits you to:
* Freely download and use bootstrap-input-prefix, in whole or in part, for personal, private, company internal, or commercial purposes
* Use bootstrap-input-prefix in packages or distributions that you create
* Modify the source code
* Grant a sublicense to modify and distribute bootstrap-input-prefix to third parties not included in the license

#### It forbids you to:
* Hold the authors and license owners liable for damages as bootstrap-input-prefix is provided without warranty
* Hold the creators or copyright holders of bootstrap-input-prefix liable
* Redistribute any piece of bootstrap-input-prefix without proper attribution
* Use any marks owned by Array Software in any way that might state or imply that Array Software endorses your distribution
* Use any marks owned by Array Software in any way that might state or imply that you created the Array Software software in question

#### It does not require you to:
* Include the source of bootstrap-input-prefix itself, or of any modifications you may have made to it, in any redistribution you may assemble that includes it
* Submit changes that you make to bootstrap-input-prefix back to the bootstrap-input-prefix project (though such feedback is encouraged)

See the LICENSE file for the full bootstrap-input-prefix license.