# _brainfuck.js_

_A simple Brainfuck interpreter written in JavaScript_

## Usage
```html
<div id="output"></div>
<script src="brainfuck.js"></script>
<script type="text/javascript">
    var program = Brainfuck('++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.'); 
    var output = document.getElementById('output');
    program.write = function(charCode) {
        output.innerHTML = output.innerHTML + String.fromCharCode(charCode);
    };
    program.run();
</script>
```

## FAQ

**1. What's this peace of crap?**

   Propably nothing you should be concerned with.

**2. Will you keep working on this?**

   Except for bugfixes, not. Look at it: it's done.

**3. Can I prevent the brainfuck program from blocking my JavaScript execution?**

   Kind of: you can provide a numerical parameter to run, specifiying the maximum number of instructions to be executed before returning from run. You can re-issue a run call at a later point, e.g. with setTimeout and keep your JavaScript execution going that way.

**4. Why is this no node module?**

   Because I wanted a Brainfuck interpreter for the browser. I might write an asynchronous, stream compatible interpreter for node at a later point. I _might_. Don't quote me on this.
