#### [chessboard.html V0.3](http://dmolinarius.github.io/www2013-css-challenge/V0.3/chessboard.html) - 8x8 B&W tiled background
<blockquote> 
Display 8 stripes resulting in tiled background. Position of stripe n is :
```
x = (n * 1/8) + x * (n * 1/8)
```
leading to : <code>x = n / 7</code> with n taking 8 values from 0 to 7
 
Tested with :
- Firefox 20.0 for Windows
- Chrome 26.0 for Windows
- Opera 12.5 for Windows
- Internet Explorer 10.0 for Windows
</blockquote>

#### [V0.2](http://dmolinarius.github.io/www2013-css-challenge/V0.2/chessboard.html) - 2 Vertical stripes of 8 black and white cells
<blockquote>
The tricky part as announced by Bert Bos during his talk, is about computing the right percentage for background-position :
```
background-position: 0 0, 14.286% 0;
```

The CSS specification at http://www.w3.org/TR/CSS2/colors.html#propdef-background-position says : 
<q>A percentage X aligns the point X% across (..) the image with the point X% across (..) the element's padding box.</q>

If our stripes are 1/8 of the total width and according to the specs, if we call x
the searched fraction we have :
```
x (fraction of the total width) = 1/8 (width of the first stripe) + x*1/8 (fraction of the second stripes's width)
```
  
which results in :
```
x = 1/7 (or 14.286 once multiplied by 100 to get % units)
```
</blockquote>

#### [V0.1](http://dmolinarius.github.io/www2013-css-challenge/V0.1/chessboard.html) - Vertical stripe of 8 black and white cells
