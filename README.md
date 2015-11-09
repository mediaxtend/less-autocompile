# less-autocompile package

_This fork is a patched version to permit [JavaScript expression evaluation](https://github.com/less/less.js/blob/master/lib/less/tree/js-eval-node.js) inside LESS source. It's using a [patched version](https://github.com/mediaxtend/less.js) of Less.js compiler and the [Eval Loophole](https://github.com/cgrabowski/loophole) hack._

Auto compile LESS file on save.

---

Add the parameters on the first line of the LESS file.

```
out (string):  path of CSS file to create
sourcemap (bool): create sourcemap file
compress (bool): compress CSS file
main (string): path to your main LESS file to be compiled
```

## Example
less/styles.less
```scss
// out: ../css/styles.css, sourcemap: true, compress: true

@import "my/components/select.less";
```

less/my/components/select.less
```scss
// main: ../../styles.less

.select {
  height: 100px;
  width: 100px;
}
```
