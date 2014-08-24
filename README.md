brainfuck.js
============

A simple Brainfuck interpreter written in JavaScript

## Usage
```html
<div id="output"></div>
<script src="brainfuck.js"></script>
<script type="text/javascript">
    var program = new Brainfuck('++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.'); 
    var output = document.getElementById('output');
    program.write = function(charCode) {
        output.innerHTML = output.innerHTML + String.fromCharCode(charCode);
    };
    program.read = function() {
        return String.charCodeAt(prompt('Input'), 0);
    };
    program.run();
</script>
```

## FAQ

**1. What's this piece of crap?**

   Probably nothing you should be concerned with.

**2. Will you keep working on this?**

   Except for bugfixes, no. Look at it: it's done.

**3. Can I prevent the brainfuck program from blocking my JavaScript execution?**

   Kind of: you can provide a numerical parameter to run, specifiying the maximum number of instructions to be executed before returning from run. You can re-issue a run call at a later point, e.g. with setTimeout and keep your JavaScript execution going that way.

**4. Why is this no node module?**

   Because I wanted a Brainfuck interpreter for the browser. I might write an asynchronous, stream compatible interpreter for node at a later point. I _might_. Don't quote me on this.

## Contributors

* Daniel Baulig ~ Main developer
* 316k ~ Small bugfix, corrected typos in README.md

## License

Copyright (c) 2012 Daniel Baulig <daniel.baulig@gmx.de>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.  IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
