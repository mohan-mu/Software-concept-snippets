I have been learning Advanced CSS with SASS, and think it's going to be really useful for building the Intygrate website. I'm pretty familiar with vanilla CSS, but not any other CSS frameworks, so I'm aware that my lack of experience will make it harder to give a balanced view in comparison to other frameworks.

Here are some of the key things SASS will be super useful for when it comes to building the website (with my opinion on potential problems):

##### 7-in-1-pattern:

The seven in one pattern is where you seperate your css into 7 different folders. Sass lets you compile them all into the main CSS file at the end. I found this to be a really intuitive way to organise files. I like that you can end up building your own component library of reusable forms, buttons, cards etc. 

The best thing about this is that it encourages you not to repeat yourself using things like mixins and variables to change colours, font sizes and media query breakpoints across the whole site in only one place. So if we need to play around with how the site looks with different font sizes and colours, it'll be really easy to do so.

My problem with this approach is that it makes you order your code into groups of what is on your page, rather than why things are grouped together in a particular way. You would have to look at the css to see which page has which set of components to get an idea of the intention behind the content of the website. 

Overall though, I am a fan of the approach and could play around with the folder grouping, though it's probably best to stick with the standard so that anyone working on it will understand where to find things if they know the model.

##### BEM model:

The bem model is where we give a class to every single element on the page using a Block__element__modifier format.

I think of blocks as a component level container, elements are the headings, paragraphs and images etc, whilst the modifiers are an extra bit of the class that lets you target things with more specificity if you need to make them look slightly different (e.g if you have two h3 tags in the same block but you want one of them to look different).


###### HTML:

```html
<div class="card card__side card__side--back card__side--back-1">
  <div class="card__cta">
    <div class="card__price-box">
      <p class="card__price-only">Only</p>
      <p class="card__price-value">$297</p>
    </div>
    <a href="#popup" class="btn btn--white">Book Now</a>
  </div>
</div>
```

###### CSS:

```css
.card {

    &__price-box {
        text-align: center;
        color: $color-white;
        margin-bottom: 8rem;
    }

    &__price-only {
        font-size: 1.4rem;
        text-transform: uppercase;
    }

    &__price-value {
        font-size: 6rem;
        font-weight: 100;
    }

}
```


###### Mixins:

The ability to make mixins is a really great benefit of Sass too. We can use them to call media queries in our css like this:
```css
@include respond(phone) {}
@include respond(tablet-port) {}
```

This is really easy to read for people, and easy to adjust in the mixin files.




I have attached a document containing all of the other things the course covered if you are interested. The key benefits that I think will be a great help in the project are what I've covered above though.
