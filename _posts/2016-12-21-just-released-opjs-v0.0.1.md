---
layout: post
title: "Just released opjs v0.0.1"
description: "a simple and lightweight Javascript library to implement SPA Architecture"
comments: true
keywords: "opjs, js, javascript, opjs v0.0.1, javascript library, js library"
---

OPJS is a simple and lightweight Javascript library to implement SPA Architecture. Its size is very small only ~3KB minified. It was written up to 231 code lines. Its benefits are that it's pure Javascript and doesn't depend on other libraries.

### Usage

In order to use it, you just include simplely it into HTML page. By my front-end experience, you should let it into end of closing body tag to improve the best performance. Secondly, you create an any element to decorate an attribute named "data-opjs-route". This attribute is used to update HTML strings coming from configuring routings. Finally, you configure routings using function opjs.config.route().

* include it into HTML page.
* add attribute "data-opjs-route" into any element.
* configure routings.

### For example

create a HTML web page with routes as follows:

* '/' or '#/': home page with template url being /partials/home.htm.
* '#/about': about page with template html being '<b>about</b>'.
* redirect_url: in case route was failed, it will be used to redirect to specified URL path.

```html
<html>
<head>
    <title>OPJS</title>
</head>
<body>
    <div id="content">
        <a href="#/">Home</a>
        <a href="#/about">About</a>
        <div data-opjs-route='route'>
        </div>
    </div>
    <script type="text/javascript" src='opjs.js'></script>
    <script>
        (function (w) {
            w.opjs.config.route({
                redirect_url: '/',
                data: [{
                    name: 'home',
                    url: '/',
                    states: [{
                        name: 'route',
                        template_html_or_url: '/partials/home.htm',
                        use_html_template: false
                    }]
                }, {
                    name: 'about',
                    url: '/about',
                    states: [{
                        name: 'route',
                        template_html_or_url: '<b>about</b>',
                        use_html_template: true
                    }]
                }]
            });
            w.opjs.bootstrap();
        })(window);
    </script>
</body>

</html>

```

### In Conclusion

I hope that you can enjoy this library. More details at: [https://github.com/hptechguy/opjs](https://github.com/hptechguy/opjs). Happy Coding!
