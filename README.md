# YSlow Explore
=====

Playing around with YSlow to see if the rules can be extracted and run by a simpler Node.js app, perhaps using simple request and JSDom. 

You can develop with the Chrom Dev Tools with: node --inspect app.js -f json http://annrobson.com/

The phantomjs version is not going to let you step deeply into it because of the way it is run with evaluate 😬. If you wanted inpect part of it you can do this, which works in Safari only:
phantomjs --remote-debugger-port=9000 yslow.js --info basic --format plain http://annrobson.com

(That would be within the build/phantomjs folder.)

99.9% of the code I did not touch (there's a lot of code). View YSlow code here: https://github.com/marcelduran/yslow

YSlow
=====

YSlow analyzes web pages and suggests ways to improve their performance based on a set of [rules for high performance web pages](http://developer.yahoo.com/performance/rules.html).

### Building

All flavors:

    make

Specific flavor:

    make <flavor>

Available flavors:

* **firefox**: Mozilla [Firefox add-on](https://addons.mozilla.org/en-US/firefox/)
* **chrome**: Google [Chrome extension](https://chrome.google.com/webstore/category/extensions)
* **bookmarklet**: Mobile/Desktop browser [bookmarklet](http://en.wikipedia.org/wiki/Bookmarklet)
* **opera**: [Opera extension](http://extensions.opera.com/)
* **safari**: Apple [Safari extension](http://extensions.apple.com/)
* **nodejs**: Command line for [HAR](http://www.softwareishard.com/blog/har-12-spec/) files powered by [Node.JS](http://nodejs.org/) and [NPM](http://npmjs.org/)
* **phantomjs**: Command line with headless [WebKit](http://www.webkit.org/) powered by [PhantomJS](http://www.phantomjs.org/)
* **nodeserver**: Node.JS Server powered by [express](http://expressjs.com/)

e.g.:

    make chrome

### Packaging

All flavors:
    
    make pkg

Specific flavor:

    make pkg-<flavor>

e.g:

    make pkg-firefox

More Info
---------

[yslow.org](http://yslow.org)

Licensing
---------

Copyright (c) 2012, Yahoo! Inc. All rights reserved.  
Copyright (c) 2013, Marcel Duran and other contributors. All rights reserved.  
Copyrights licensed under the New BSD License. See the accompanying LICENSE file for terms.


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/marcelduran/yslow/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

