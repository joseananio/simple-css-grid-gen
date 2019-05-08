#Simple CSS Grid Generator.

This is not meant to be a full stack like Bootstrap grid and other, but to provide a quick and simple grid to add in your project if you only need quick grids that are responsive.

Bootstrap has more functionality than this and it is recommended if you wat a full stack grid.

## Usage

```html
<div>
    <div class="row">
        <div class="sm-2 md-6 lg-10 a">this is so simple</div>
        <div class="sm-10 md-6 lg-2 b">And fun</div>
    </div>
    <div class="row">
        <div class="c">full width column</div>    
        <div class="a">Another full width column</div>    
    </div>

    <div class="row">
        <div class="sm-2 md-4 lg-3 e">this is so simple</div>
        <div class="sm-5 md-4 lg-2 d">And fun</div>
        <div class="sm-5 md-4 lg-7 c">And fun</div>
    </div>
</div>
```
```css
/* sample css*/
.row > div {
  height: 100px;
  text-align: center;
  padding: 10px;
  padding-top: 35px;
  line-height: 30px;
  font-size: 18px;
}
.row > div.a {
  background: #011936;
  color: #a5bad4;
}
.row > div.b {
  background: #465362;
}
.row > div.c {
  background: #82A3A1;
}
.row > div.d {
  background: #9FC490;
}
.row > div.e {
  background: #C0DFA1;
}
```
  [![Sample](https://github.com/joseananio/simple-css-grid-gen/blob/master/resources/output.gif)]



## Workings

 - Uses `.row` to create a horizontal row, and then goes straight to column classes. No need to add `.col` class or prefix.

 - Each `div` directly inside a `.row` element is automatically considered to be a column.

 - Uses box-sizing: border-box and no margins on rows and columns.

- Output is about 5kB uncompressed.

## Dev

 - To genereate output css, run:

    `
    ./node_modules/.bin/sass --watch ./styles.scss ./dist/output.css
    `

 - Modify `$screen-sizes` in style.scss if yo want different grid sizes.

 Default screen sizes correspond to bootstrap sizes.


 Todo: Push, pull and offset 
