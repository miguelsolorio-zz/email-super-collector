# Email Super Collector
This email collector is created to enhance collecting email addresses from your customers. Once integrated into your website, your users will be prompted with a lightbox that asks them if they would like to be added to your subscription list. Once the user has been prompted with the lightbox, they will not be asked again until the Super Collector cookie expires.

You have the ability to customize the style of the content, designate the expiration date of the cookie, and the timer used to initialize the Super Collector. For this Demo page, the Super Collector will run after 5 seconds.

This plugin utilizes the following libraries:
- [jQuery](http://jquery.com/)
- [jQuery Cookie](https://github.com/carhartl/jquery-cookie.git)
- [Colorbox](http://www.jacklmoore.com/colorbox/)

### Configuration
```javascript
$(document).ready(function(){
  // set timer in ms
  var superCollectorTime;
  superCollectorTime = setTimeout(initBox, 100000);
  function initBox(){
    // If there is no cookie, initialize colobox poup using an html link
    if ($.cookie('superCollectorCookie') != '1'){
      $.colorbox({href:"supercollector.html",iframe:true, width:"450px", height:"350px"});
      // add cookie and expiration days
      $.cookie('superCollectorCookie', '1', { expires: 1 });
    }
  }
});
```

### Demo Page
- [miguelsolorio.github.io/email-super-collector/](http://miguelsolorio.github.io/email-super-collector/)