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
			outCssPath: './dest/css/',
			outImgPath: './dest/images/',
			padding: 10
		})
	];
	return gulp.src('src/postcss/*.css')
		.pipe(postcss(processors))
		.pipe(gulp.dest('/dest/css/'));
});
```