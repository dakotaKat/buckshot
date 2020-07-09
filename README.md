# buckshot
Buckshot, the Pigeon Paywall killer for NorthCountryNow.com

Basic extension that does the following things:

## Blocks web requests to my.northcountrynow.com
my.NCN hosts the subscription management and Pigeon paywall scripts. Let's just axe that in the bud right here. Killing all web requests to my.NCN also keeps the subscription bar from appearing (as expected), blocks Incognito detection (*if browser set to allow extension in Incognito), etc.

Theoretically, this could be removed from the extension and the host blocked via other means (ie Adblock filters, Host filtering, etc).

## Unhides protected content
The Pigeon paywall software blocks access to content via HTML `div`s that have their property set to `visible: hidden`. The content.js script in my extension forces all of those back to `inline` so that they're viewable once the page is done loading. I'm sure I could do this without JQuery, but I'm fast and lazy, and I don't really know Javascript in the first place.
