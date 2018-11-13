#### [chessboard.html V0.4](http://dmolinarius.github.io/www2013-css-challenge/V0.4/chessboard.html) - Centered chessboard
<blockquote>
Centered Chessboard using CSS3 viewport percentage units, anc calc(), see :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;http://www.w3.org/TR/css3-values/#viewport-relative-lengths<br/>
&nbsp;&nbsp;&nbsp;&nbsp;http://www.w3.org/TR/css3-values/#calc<br/>
<br/>

Tested with :
- Firefox 20.0 for Windows ... [[OK]](http://dmolinarius.github.io/www2013-css-challenge/V0.4/V0.4%20Firefox.png)

- Internet Explorer 10.0 for Windows ... [[partially OK]](http://dmolinarius.github.io/www2013-css-challenge/V0.4/V0.4%20IE10.png)
  - chessboard properly centered, but no box-shadow :
        viewport units and calc() are not recognized in the
        context of box-shadow, even if those are properly interpreted
        to center the chessboard...

- Chrome 26.0 for Windows ... [[partially OK]](http://dmolinarius.github.io/www2013-css-challenge/V0.4/V0.4%20Chrome.png)
  - displays rounding error at bottom of chessboard
  - properly scales the chessboard but doesn't position it properly
     (flags an invalid value for top and left)
  - no box-shadow

- Opera 12.5 for Windows ... [[NOT OK]](http://dmolinarius.github.io/www2013-css-challenge/V0.4/V0.4%20Opera.png)
  - chessboard not centered, no box shadow
     (does not implement viewport units nor calc())
</blockquote>

#### [V0.3](http://dmolinarius.github.io/www2013-css-challenge/V0.3/chessboard.html) - 8x8 chessboard background
<blockquote>
Display 8 stripes resulting in tiled background. Position of stripe n is :

```
x = (n * 1/8) + x * (n * 1/8)
```

leading to : <code>x = n / 7</code> with n taking 8 values from 0 to 7.

Tested with :
- Firefox 20.0 for Windows ... [OK]
- Opera 12.5 for Windows ... [OK]
- Internet Explorer 10.0 for Windows ... [[OK]](http://dmolinarius.github.io/www2013-css-challenge/V0.3/V0.3%20IE10.png)
- Chrome 26.0 for Windows ... [[partially OK]](http://dmolinarius.github.io/www2013-css-challenge/V0.3/V0.3%20Chrome.png)
  - displays rounding error at bottom of chessboard
</blockquote>

#### [V0.2](http://dmolinarius.github.io/www2013-css-challenge/V0.2/chessboard.html) - 2 stripes of 8 black and white cells
<blockquote>
The tricky part as announced by Bert Bos during his talk,
    is about computing the right percentage for background-position :

```
background-position: 0 0, 14.286% 0;
```

According to the CSS specification http://www.w3.org/TR/CSS2/colors.html#propdef-background-position :
<q>A percentage X aligns the point X% across (..) the image with the point X% across (..) the element's padding box.</q>

If our stripes are 1/8 of the total width and calling x the searched fraction we have :

```
      1/8 (width of the first stripe)
+ x * 1/8 (fraction of the second stripes's width)
= x (fraction of the total width)
```
  
which results in <code>x = 1/7</code> (or 14.286 once multiplied by 100 to get % units)
</blockquote>

#### [V0.1](http://dmolinarius.github.io/www2013-css-challenge/V0.1/chessboard.html) - Vertical stripe of 8 black and white cells
