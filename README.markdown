# Minitemplate

A tiny, secure JavaScript minitemplating function.

It lets you write simple templates that uses JavaScript's familiar dot notation. You pass in a JavaScript object that contains all the relevant strings, and they are then substituted into the template. For example:

    minitemplate("Hello {{place}}", {place: "world"});
    // "Hello world"

* Forked from: [github.com/premasagar/tim](http://github.com/premasagar/tim) ([MIT license](http://opensource.org/licenses/mit-license.php))
* Apps using it this function are easily upgradable to use the full version of tim,Mustache, underscore and other template engines if more functionality is needed

## Why is minitemplating useful?
Don't you just hate having to write HTML with a mess of string concatenation that clutters up your JavaScript?:

    var myHTML = "<ul class='" + myClass + "'>" +
        "<li id='" + theId + "'>" + liContents + "</li>" +
        // etc, etc, etc
        
Yuck. There's no need to do this. Simply prepare a JavaScript object with the required properties, and inject it into a simple template string. The templates can all be tidily kept together with the rest of the markup in an HTML document.


## How is this different from other templating scripts?
It is safe and secure: it doesn't use eval or (new Function), so it cannot execute malicious code. As such, it can be used in secure widgets and apps that disallow eval - e.g. Adobe Air sandboxes, AdSafe ads, etc.

It doesn't include a whole bloat load of features that are unlikely to get used when you just want to get some simple templating up and running.
