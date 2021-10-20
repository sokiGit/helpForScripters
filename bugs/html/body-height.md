# Body height bug

### This bug causes the body height not to 100% fill the page.

*How does this happen?*
> This happens when you set the *Class* or *ID* of an element other than the *body* element to *"body"* and set the class `.body` a height. That will look like this (CSS): `.body {height: 200px;}`

*How does this look?*
> You code will look something like this:
```html
<!-- This is the wrong code. -->
<!DOCTYPE html>
<html>
  <head>...<head>
  <body>
    <element class="body">...</element>
  </body>
</html>
```

*How do I fix this?*
> You have to rename the class name to something else (I personally recomment something like *"container"*) and you must edit the class name in the CSS code to match that class name.
```html
<!DOCTYPE html>
<html>
  <head>...</head>
  <body>
    <element class="container"<!--OR ANY OTHER NAME THAN AN ELEMENT NAME--> >...</element>
  </body>
</html>
```
> Now just set the height and width of the `html` and `body` element. This is in the *CSS* language
```css
hmtl, body {
  height: 100%;
  width: 100%;
}
```

*Grepper answer:*
```html
<!--

This is caused by a class name being set to "body". This can be applied to any other element!
For example:
  <div class="body"> - This is the WRONG code! Becouse "body" is a name of an element.
  <div class="container"> - This is the RIGHT code! Becouse "container" is not a name of an element.

Now just do this in your css code:
html, body {
  height: 100%;
  width: 100%;
}

 !! Better explanation on github: sokiGit/helpForScripters/bugs/html/body-height.md

-->
```
