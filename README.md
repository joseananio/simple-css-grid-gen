 Simple CSS grid generator.

## Usage

```html
<div class="row">
    <div class="sm-2 md-6 lg-10 xs-9">this is so simple</div>
    <div class="sm-10 md-6 lg-2 xs-3">And fun</div>
</div>
<div class="row">
    <div>full width column</div>    
    <div>Another full width column</div>    
</div> 
```
```css
/* sample css*/
.row >div{
    height: 50px;
    text-align: center;
    padding: 5px;
    padding-top: 10px;
    line-height: 30px;
    // border: 1px solid #333;
    &.a{
        background: rgb(194, 23, 23);
    }
    &.b{
        background: rgb(207, 207, 6);
    }
    &.c{
        background: rgb(12, 172, 12);
    }
    &.d{
        background: rgb(150, 16, 150);
    }
}
```
  [![Sample](https://github.com/joseananio/simple-css-grid-gen/blob/master/resources/output.gif)]


## Workings

This uses `.row` to create a horizontal row, and then goes straight to column classes. No need to add `.col` class or prefix.

There is however a `.col` class than can be used alone as an alias for col-12 for all screen sizes.

## Dev

 To genereate output css, run:

 `
 ./node_modules/.bin/sass --watch ./styles.scss ./dist/output.css
 `

 Modify `$screen-sizes` in style.scss if yo want different grid sizes.

 Default screen sizes correspond to bootstrap sizes.


 Todo: Push, pull and offset 
