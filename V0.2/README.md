#### [chessboard.html V0.2](http://dmolinarius.github.io/www2013-css-challenge/V0.2/chessboard.html) - 2 Vertical stripes of 8 black and white cells
<blockquote>
Draws 2 stripes of 8 black and white cells, which have 1/8 of the window width.<br/><br/>

Tested with :
- Firefox 20.0 for Windows
- Chrome 26.0 for Windows
- Opera 12.5 for Windows
- Internet Explorer 10.0 for Windows

The tricky part as announced by Bert Bos during his talk, is about computing the right percentage for background-position :
```
    background-position: 0 0, 14.286% 0;
```

The CSS specification at http://www.w3.org/TR/CSS2/colors.html#propdef-background-position says : 
<q>A percentage X aligns the point X% across (..) the image with the point X% across (..) the element's padding box.</q>

If our stripes are 1/8 of the total width and according to the specs, if we call x
the searched fraction we have :
```
x (fraction of the total width) = 1/8 (width of the first stripe) + x * 1/8 (fraction of the second stripes's width)
```
  
which results in :
```
x = 1/7 (or 14.286 once multiplied by 100 to get % units)
```
</blockquote>
