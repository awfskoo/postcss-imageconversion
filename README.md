# postcss-imageconversion


## Base64

https://github.com/jelmerdemaat/postcss-base64


## easysprites

https://github.com/glebmachine/postcss-easysprites


```
gulp.task('postcss', function() {
	var processors = [
		imageconversion({
			extensions: ['.png', '.jpg'],
			maxSize: 15,
			imagePath: './src/images/',
			stylesheetPath: './src/postcss/',
			spritePath: '/images/sprite/',
			padding: 2
		})
	];
	return gulp.src('src/postcss/*.css')
		.pipe(postcss(processors))
		.pipe(gulp.dest('/dext/css/'));
});
```