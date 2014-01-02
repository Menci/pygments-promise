pygments-async
==============

Fully asynchronous wrapper for Pygments

## Usage

There are two functions exported by the package - pygmentize and pygmentizeFile.

### pygmentize

Highlight a block of code

Example:

```javascript
var pygmentize = require('pygments-async').pygmentize
  , markup;

pygmentize("puts 'Hello, world!'", {lexer: 'ruby'}, function(err, out) {
  // out contains pygmentized code
  markup = out;
});
```

Allowed options are:

- `lexer`: Specify lexer for pygmentize
- `formatter`: Specify pygmentize lexer

Options need not be specified. If no lexer is provided pygmentize will attempt
to guess based on contents. The default formatter is `html`.

### pygmentizeFile

Load a file and pygmentize it

```javascript
var pygmentize = require('pygments-async').pygmentize
  , markup;

pygmentizeFile("package.json", function(err, out) {
  // out contains pygmentized package.json
  markup = out;
});
```

## License

MIT

## Alternatives
- [pygments](https://github.com/pksunkara/pygments.js)
