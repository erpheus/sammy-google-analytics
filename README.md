# Sammy.js Google Analytics Plugin


## Description

A small plugin that enables Google Analytics tracking for your Sammy powered App.

## Installation

Download sammy.googleanalytics.js and install it in your public javascripts directory.
Include it in your document AFTER sammy.

## Usage

Install Google Analytics to your site as you normally would.  Be sure that the 'pageTracker' global variable exists (unless you are using analytics.js instead of ga.js. In that case no additional configuration is required).

Then, simply add the plugin to your Sammy App and it will automatically track all of your routes in Google Analytics.  They will appear as page views to the route's path.

    $.sammy(function() { with(this) {
      use(Sammy.GoogleAnalytics)
      
      ...
    }});

If you have routes that you do not want to track, simply call "noTrack" within the route.

    $.sammy(function() { with(this) {
      use(Sammy.GoogleAnalytics)
      
      get('#/dont/track/me', function() {
        this.noTrack();  // This route will not be tracked
      });
    }});

## Example

[http://britg.github.com/sammy-google-analytics](http://britg.github.com/sammy-google-analytics)


## Dependencies

Sammy [http://code.quirkey.com/sammy](http://code.quirkey.com/sammy)

Sammy requires jQuery >= 1.3.2
Get it from: [http://jquery.com](http://jquery.com)

## More!

### Learn!

* [Intro](http://code.quirkey.com/sammy)
* [Docs](http://code.quirkey.com/sammy/docs/)
* [Examples](http://github.com/quirkey/sammy/tree/master/examples/)
* [More Resources](http://code.quirkey.com/sammy/resources.html)

### Keep informed!

* [Follow @sammy_js](http://twitter.com/sammy_js)
* [Join the mailing list](http://groups.google.com/group/sammyjs)
* [Chat with us in #sammy](irc://irc.freenode.net/#sammy)

## License

Sammy is covered by the MIT License. See LICENSE for more information.

Sammy includes code originally created by John Resig ([Class implementation](http://ejohn.org/blog/simple-javascript-inheritance/)) and Greg Borenstien ([srender](http://github.com/atduskgreg/srender/tree/master)).
