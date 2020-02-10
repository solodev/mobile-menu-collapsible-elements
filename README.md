# mobile-menu-collapsible-elements
Simply because of the restraints of a smaller device, mobile menus can’t show all navigational items. For large sites, however, this can pose a challenge. One way to circumvent this is by adding collapsible elements to your mobile menu items.

## Tutorial
For detailed instruction's, view Solodev's [How to add collapsible elements to your mobile menu](http://www.solodev.com/blog/web-design/how-to-add-collapsible-elements-to-your-mobile-menu.stml) article.

## Demo
Try out a working example on [JSFiddle](https://jsfiddle.net/solodev/3sjxkLda/).

## HTML
The tutorial contains the following basic HTML markup.

```
 <div class="header navigation">
   <div class="col-xl-3 col-lg-2 col-sm-4 col-5">
     <a href="/">
       <img alt="Logo" class="img-fluid py-3 logo" src="https://raw.githubusercontent.com/solodev/mobile-menu-collapsible-elements/master/images/lunarxp-logo-white.png" aria-role="logo">
     </a>
   </div>
 </div>
 <div id="overlay" class="overlay hidden" role="navigation">
   <div class="wrap box-wrap">
     <div class="mobileNav black;">
       <div class="box-close box-toggle open2">
         <a href="#" class="toggle-mobile" aria-label="Menu Toggle">×</a>
       </div>
       <div class="box-mobile-menu mobile-menu">
         <div class="mobile-menu mt-1">
           <div class="mobile-tab position-relative mb-4">
             <h3 class="h4 tab">Trip Tools</h3>
             <ul class="pl-4 my-4 nolist">
               <li><a href="#" aria-label="Trip Apps Link">Trip Apps</a></li>
               <li><a href="#" aria-label="Trip Planner Link">Trip Planner</a></li>
               <li><a href="#" aria-label="Space Excursions">Space Excursions</a></li>
             </ul>
           </div>
           <h3 class="h4 mb-4"><a href="#" aria-label="Buy SpeceJet Tickets">Buy SpeceJet Tickets</a></h3>
           <div class="mobile-tab position-relative mb-4">
             <h3 class="h4 tab">Maps &amp; Schedules</h3>
             <ul class="pl-4 my-4 nolist">
               <li><a href="#" aria-label="Routes & Schedules Link">Routes &amp; Schedules</a></li>
               <li><a href="#" aria-label="Map Gallery Link">Map Gallery</a></li>
               <li><a href="#" aria-label="Popular Destinations Link">Popular Destinations</a></li>
               <li><a href="#" aria-label="Interactive Maps Link">Interactive Maps</a></li>
             </ul>
           </div>
           <h3 class="h4 mb-4"><a href="#" aria-label="Contact Link">Contact</a></h3>
         </div>
         <hr>
       </div>
       <!--.mobile-menu-->
     </div>
   </div>
 </div>
```
## Javascript
```
$('.toggle-mobile').click(function() {
  $('.overlay').toggleClass('hidden');
});

$('.mobile-tab').on('click', 'h3', function(e) {
  $(this).toggleClass('active');
  $(this).parent().find('ul').toggleClass('open');
  e.preventDefault();
});
```

## CSS
All required CSS is contained with style.css

## External Resources
This tutorial includes the following third party resources.

```
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
```
