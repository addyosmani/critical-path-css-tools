Critical-path CSS Tools
=========================

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


## Inline styles

* [inline-styles](https://github.com/maxogden/inline-styles) - by Max Ogden replaces link tags with inline style tags + inlines CSS url() calls with data URIs

## Async load CSS

Async loading should be used to fetch the rest of your site-wide styles after you've inlined your critical-path CSS.

* [loadCSS](https://github.com/filamentgroup/loadCSS) - loads CSS asynchronously using JS. [Research](https://gist.github.com/scottjehl/87176715419617ae6994) that led to this is also available.

## Online tools

* [Penthouse online](http://jonassebastianohlsson.com/criticalpathcssgenerator/)

## Bookmarklets/Extensions

* [Snippet](https://gist.github.com/PaulKinlan/6284142) by Paul Kinlan
* [Snippet](https://gist.github.com/scottjehl/b6129da04733e4e0f9a4) by Scott Jehl
* [CSSVacuum](https://github.com/ndreckshage/CSSVacuum) by ndreckshage
