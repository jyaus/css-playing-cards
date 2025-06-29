CSS Playing Cards
=================
- by Jeff Yaus

Playing cards using only CSS and Unicode characters

[http://jyaus.github.io/css-playing-cards/](http://jyaus.github.io/css-playing-cards/)

Usage
-----     
Each card is just <code>&lt;div class="card"&gt;</code>, with two empty <code>&lt;span aria-hidden="true"&gt;</code> tags inside it. 
Each card then also gets a class for the name of the suit (e.g. <code>"card-hearts"</code>) and a class for the value 
(e.g. <code>"card-9"</code> for a nine). For instance, the king of spades would look like: 
<pre><code>
    &lt;div class="card card-spades card-k"&gt;
        &lt;span aria-hidden="true"&gt;&lt;/span&gt;
        &lt;span aria-hidden="true"&gt;&lt;/span&gt;
    &lt;/div&gt;
</code></pre>
    
A class of <code>"card-joker"</code> creates a joker; for games that need to differentiate between the two jokers, 
you can use <code>"card-joker"</code> and <code>"card-joker-alt"</code>.
    
Additionally, adding class <code>"card-facedown"</code> to a card hides its face and shows the back of the card instead.

Customizing
-----------
All the dimensions and font sizes are built using ems as the unit, so you can easily adjust the size of the deck by adjusting the base font size of the .card class.

The colors and icons used for the suits, and the names of the face cards, are stored as CSS custom properties. 
These can be easily adjusted to customize the deck from its French-style default. For instance, changing one variable will turn hearts into the 
roses used instead in a Swiss German deck; another variable will turn those roses from red to Swiss German yellow.

Accessibility
-------------
Version 3.0 of these cards is accessible and screen-reader-friendly. 

If accessibility is not a priority for you, well, shame on you,
but you can leave off the <code>aria-hidden="true"</code> on the <code>span</code> tags and thus simplify your API
to just <br />
<code>&lt;div class="card card-spades card-k"&gt;&lt;span&gt;&lt;/span&gt;&lt;span&gt;&lt;/span&gt;&lt;/div&gt;</code>

Version History
---------------
* Version 3.0 (2025 June 29):
  - full accessibility support
  - new API to support a11y; each card now needs two inner span tags, each with aria-hidden="true"
  - rewrite of the CSS to use CSS custom properties instead of LESS

* Version 2.0 (2015):
  - added some basic accessibility support

* Version 1.0:
  - initial commit
