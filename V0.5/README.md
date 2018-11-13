#### [chessboard.html V0.5](http://dmolinarius.github.io/www2013-css-challenge/V0.5/chessboard.html) - Centered chessboard with row and column annotations
<blockquote>
Row and column labels are decoration, not content. For that reason
    choice has been made to implement them using CSS. Annotations are
    created with before: and after: pseudo-elements and positioned
    and dimensioned using CSS3 units.

Since it is impossible to have multiple :before or :after
    pseudo-classes, an additional div embedding the chessboard is needed.

Tested with :

- Firefox 20.0 for Windows ... [[OK]](http://dmolinarius.github.io/www2013-css-challenge/V0.5/V0.4%20Firefox.png)

- Internet Explorer 10.0 for Windows ... [[almost OK]](http://dmolinarius.github.io/www2013-css-challenge/V0.5/V0.5%20IE10.png)
  - chessboard shadow missing [(see V0.4)](http://dmolinarius.github.io/www2013-css-challenge/V0.4/V0.4%20IE10.png)

- Chrome 26.0 for Windows ... [FAIL]
  - chessboard not centered,
  - no shadow,
  - annotations not positioned,
  - wrong font size

- Opera 12.5 for Windows ... [FAIL]
  - chessboard not visible (no size),
  - not positioned,
  - no shadow,
  - annotations not positioned,
  - wrong font size...
</blockquote>

#### [V0.4](http://dmolinarius.github.io/www2013-css-challenge/V0.4/chessboard.html) - Centered chessboard
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
