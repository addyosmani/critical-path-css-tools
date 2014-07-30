Above-the-fold CSS Tools
==========================================

> Tools to help prioritize above-the-fold CSS

### Prioritize above-the-fold content first.

For best performance, PageSpeed Insights [recommends](https://developers.google.com/speed/docs/insights/PrioritizeVisibleContent) inlining the critical (above-the-fold) CSS of your page directly into your HTML. This eliminates additional roundtrips and allows the browser to paint the above-fold experience to your user's screen sooner. The main idea is:

* Determine the above-the-fold styles for a page and write them between `<style>` tags in the head.
* Load all other stylesheets in the footer, ideally asynchronously.

The following is a list of tools to help generate, inline and report on critical-path CSS.

## Node modules


* [Penthouse](https://github.com/pocketjoso/penthouse) - by Jonas Ohlsson generates critical-path CSS
* [Critical](http://github.com/addyosmani/critical) - by Addy Osmani generates & inlines critical-path CSS (uses Penthouse, [Oust](http://github.com/addyosmani/oust) and inline-styles)
* [CriticalCSS](https://github.com/filamentgroup/criticalcss) - by FilamentGroup finds & outputs critical CSS


## Server-side modules

* [mod_pagespeed](https://code.google.com/p/modpagespeed/) - Apache module for automatic PageSpeed optimization
* [ngx_pagespeed](https://github.com/pagespeed/ngx_pagespeed) - Nginx module for automatic PageSpeed optimization

## Grunt tasks

* [grunt-penthouse](https://github.com/fatso83/grunt-penthouse)
* [grunt-critical-css](https://github.com/filamentgroup/grunt-criticalcss)


## CasperJS

* [critical-css-casperjs](https://github.com/ibrennan/critical-css-casperjs) - CasperJS script to pull critical CSS information from pages

## PhantomJS

* [dr-css-inliner](https://github.com/drdk/dr-css-inliner) - PhantomJS script to inline above-the-fold CSS on a page.

## Inline sources (styles, scripts)

* [inline-styles](https://github.com/maxogden/inline-styles) - by Max Ogden, replaces `<link>` tags with inline `<style>` tags + inlines CSS url() calls with data URIs
* [gulp-inline-source](https://github.com/fmal/gulp-inline-source) - by Filip Malinowski, replaces `<link>` tags with inline `<style>` tags, and replaces `<script src="">` tags with their inline content

## Async load CSS

Async loading should be used to fetch the rest of your site-wide styles after you've inlined your critical-path CSS.

* [loadCSS](https://github.com/filamentgroup/loadCSS) - loads CSS asynchronously using JS. [Research](https://gist.github.com/scottjehl/87176715419617ae6994) that led to this is also available.
* [async & conditional loading](https://gist.github.com/matt-bailey/602b40c77a5d3381ff26) - POC script for loading CSS files asynchronously and conditionally based on body tag classes
* [asyncLoader](https://github.com/n0mad01/asyncLoader) - async script/stylesheet loader
* [basket.js](http://addyosmani.github.io/basket.js/) - async script/resource loader with support for localStorage caching. Can be [extended](https://github.com/andrewwakeling/basket-css-example) to load stylesheets.

Note: The Guardian currently also cache their global styles into localStorage for subsequent page loads. More info in this [comment](https://gist.github.com/scottjehl/87176715419617ae6994).

## Online tools

* [Penthouse online](http://jonassebastianohlsson.com/criticalpathcssgenerator/)

## Bookmarklets/Extensions

* [Snippet](https://gist.github.com/PaulKinlan/6284142) by Paul Kinlan. Patrick Hamann has an [exercise](http://patrickhamann.com/workshops/performance/tasks/2_Critical_Path/2_2.html) using the snippet you can try out.
* [Snippet](https://gist.github.com/scottjehl/b6129da04733e4e0f9a4) by Scott Jehl
* [CSSVacuum](https://github.com/ndreckshage/CSSVacuum) by ndreckshage

## Render-blocking issues detection

* [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights) - Online tool that measures the performance of a page for mobile devices and desktop devices. It fetches the url twice, once with a mobile user-agent, and once with a desktop-user agent. 
* [PSI](http://github.com/addyosmani/psi) - Node module for PageSpeed Insights reporting as part of your build process. Use directly with Gulp or use [grunt-pagespeed](https://github.com/jrcryer/grunt-pagespeed) if a Grunt user. For local testing, a write-up using this task and [ngrok](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/) is available.
* [PageSpeed Insights DevTools extension](https://chrome.google.com/webstore/detail/pagespeed-insights-by-goo/gplegfbjlmmehdoakndmohflojccocli?hl=en) - Chrome extension for running PageSpeed tests from inside the browser.
* [PageSpeed Insights Checker for mobile extension](https://chrome.google.com/webstore/detail/pagespeed-insights-checke/mkjmodmicmpjedhoekkmafdgpocdkbna?hl=en) - checks Mobile PageSpeed score for every page and gives you a handy preview.

## Supplementary tools

* [UnCSS](https://github.com/giakki/uncss) removes unused CSS from pages, allowing you to reduce the global CSS you may need to load in for your site. Tasks are available for [Grunt](https://github.com/addyosmani/grunt-uncss), [Gulp](https://github.com/ben-eb/gulp-uncss) and [other](http://addyosmani.com/blog/removing-unused-css/) build tools.

