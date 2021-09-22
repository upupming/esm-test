# esm test

Just a test for es modules behavior in browser:

`index.html`:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <script src="b.js" type="module"></script>
    <script type="module">
      import { c } from './c.js';
      c();
    </script>
  </body>
</html>

```

`a.js`:

```js
export const a = () => alert('a')

```

`b.js`:

```js
import { a } from './a.js'

a()

```

`c.js`:

```js
export const c = () => alert('c')

```

You will see `alert(a)` and `alert(c)` in order in your browser.

## Ref

1. https://stackoverflow.com/questions/43817297/inlining-ecmascript-modules-in-html
