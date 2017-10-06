# gulp-iconfont-sass
> Create a CSS from fonts with [Gulp](http://gulpjs.com/).

## Usage

First, install `gulp-iconfont-sass` as a development dependency:

```shell
npm install --save-dev gulp-iconfont-sass
```

Then, add it to your `gulpfile.js`:

```javascript
var iconfont = require('gulp-iconfont');
var sass = require('gulp-iconfont-sass');

gulp.task('Iconfont', function(){
  gulp.src(['assets/icons/*.svg'])
    .pipe(sass({
      
    })
    .pipe(iconfont({
      fontName: 'myfont', // required
      appendCodepoints: true // recommanded option
     }))
    .pipe(gulp.dest('www/fonts/'));
});
```

`gulp-iconfont-sass` suits well with `gulp-iconfont` but you can use it in a
 more modular fashion by directly useing `gulp-svgicons2svgfont`,
 `gulp-svg2tff`, `gulp-ttf2eot` and/or `gulp-ttf2woff`.

## API

### sass(options)

#### options.template
Type: `String`

The template path (required).

#### options.ouputfile
Type: `String`

The json path (required).

