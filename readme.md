# grunt-bower-install

> Inject your Bower dependencies right into your HTML from Grunt.

## what this is.
[Grunt](http://gruntjs.com) is great.

[Bower](http://bower.io) is great.

**And now they work great together.**

`grunt-bower-install` is a Grunt plug-in, which finds your components and injects them directly into the HTML file you specify.

Whether you're already using Bower and Grunt, or new to both, `grunt-bower-install` will be easy to plug in, as you can see in the steps below.

_**do note**: Bower is still a young little birdy, so things are changing rapidly. Authors of Bower components must follow certain conventions and best practices in order for this plug-in to be as accurate as possible. It's not a perfect world out there, so needless to say, some Bower components may not work as well as others._

## Getting Started

Install the module:
```
npm install grunt-bower-install --save-dev
```

Include the task in your Gruntfile:
```js
grunt.loadNpmTasks('grunt-bower-install');
```

Create a config block within your Gruntfile:
```js
'bower-install': {
  // Point to the html file that should be updated
  // when you run `bower-install`
  html: 'app/index.html',

  // Optional:
  // If your scripts shouldn't contain a certain
  // portion of a url, it can be excluded
  ignorePath: 'app/'
}
```

Pop this in your HTML file:
```html
<!-- bower -->
<!-- endbower -->
```

Install a Bower component:
```
grunt bower-install:jquery
```

You're in business!
```html
<!-- bower -->
<script src="bower_components/jquery/jquery.js"></script>
<!-- endbower -->
```

If you want to uninstall a Bower component:
```
grunt bower-uninstall:jquery
```

## Examples
A simple sample apple:
[website](http://stephenplusplus.github.io/grunt-bower-install) | [github](https://github.com/stephenplusplus/grunt-bower-install/tree/gh-pages)

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## License
Copyright (c) 2013 Stephen Sawchuk
Licensed under the MIT license.