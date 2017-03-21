# animated-scroll-down-anchor
Using [Animate.css](https://daneden.github.io/animate.css/), you can create a number of effects that are both visually appeasing and consistent within the world of UX/UI design. In conjunction with an suitable anchor arrow, an animated class can immediately convey to a user that their next point of action should be clicking this specific object. This helps designers and developers better control the user flow and make sure important content is appropriately shown to a given user.

In this tutorial, we will teach you how to add an animated scroll down anchor that utilizes the "bouncy" animation class. Using JavaScript, we attached a 5-second interval to the animation that continues infinitely.
## Tutorial

For detailed instruction's, view Solodev's [Adding an Animated Scroll Down Anchor](https://www.solodev.com/blog/web-design/adding-an-animated-scroll-down-anchor.stml) article.

## Demo

Try out a working example on [JSFiddle](https://jsfiddle.net/solodev/ufxtcg8v/).

## HTML

The animated scroll anchor contains the following basic HTML markup.

```
<section class="image-hero">
  <div class="image-center image-hero-content white">
    <div class="container">
      <h1 class="white">Big Data.<br />Realtime Insight.</h1>
      <p class="white">Leverage your data and improve marketing and sales ROI. WebCorpCo is at the forefront of digital marketing, content management, automated marketing, and more.</p>
    </div>  
  </div>
  <a class="ct-btn-scroll ct-js-btn-scroll animated" href="#scrollDown"></a>
</section>

<section id="scrollDown">
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="ct-content ct-sectional-content">
          <div class="inner text-center">
            <h2 class="ct-section-header">
              How It Works
            </h2>
			<h3>Learn How to Add a Bouncy Scroll Down Anchor</h3>
			<p>The main components of a bouncy scroll down anchor are made by possible by Animate.css in conjunction with some basic JavaScript. Animate.css is used to provide the foundation of the animation, where as JavaScript is used to both control the interval of the animation as well as create the scrolling anchor functionality.</p>
			<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
			<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

## CSS

All required CSS is in animated-scroll-anchor.css

## JavaScript

The animated scroll anchor is initiated by the following JavaScript.

```
$(document).ready(function(){
  $(".ct-btn-scroll").on('click', function(event) {
    if (this.hash !== "") {
      event.preventDefault();
      var hash = this.hash;
      $('html, body').animate({
        scrollTop: $(hash).offset().top
      }, 800, function(){
        window.location.hash = hash;
      });
    } 
  });
    
  setInterval(function(){
    $('.ct-btn-scroll').toggleClass("bounce");
  }, 5000);    
    
});
```

## External Resources

This tutorial includes the following third party resources.

```
<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
<link href="animated-scroll-anchor.css" rel="stylesheet">
<link href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.5.2/animate.min.css" rel="stylesheet">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<script src="animated-scroll-anchor.js"></script>
```
