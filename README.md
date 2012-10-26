The Responsive Images WebCore fork!!!
--------------------

This repository contains experiments in adding the `<picture>` element to
WebKit's WebCore library.

It is based on Chromium's WebKit from 17/10/12.

*Note*: This is a work in progress. It does not (yet) represent a full
implementation of the `<picture>` element [specification](http://responsiveimagescg.github.com/picture-element/). Please file any
inconsistency with the specification as an issue.


Build instructions:
----------------------
* Build Chromium like you normally would on [Linux](http://code.google.com/p/chromium/wiki/LinuxBuildInstructions) or [OSX] (http://code.google.com/p/chromium/wiki/MacBuildInstructions)
* If your time is precious, use [Ninja](http://code.google.com/p/chromium/wiki/NinjaBuild)
* Download the patch from [here](https://raw.github.com/yoavweiss/RespImg-WebCore/master/picture_patch.txt) to your /tmp directory
* Apply the patch using `(cd third_party/WebKit/Source/WebCore && patch -p0 < /tmp/picture_patch.txt)`

Binaries:
--------------------------
* Ubuntu 64bit & OSX binaries can be found [here]( https://github.com/yoavweiss/RespImg-WebCore/downloads)

Test page:
---------------------
Once you got your new binary, you can see `<picture>` in action [here] (http://yoavweiss.github.com/RespImg-WebCore/)

What should be working:
--------------------
* `<picture><source src></picture>` should work. The *first* source
  should be fetched by the PreloadScanner and then displayed when the
element is parsed.
* `<picture src></picture>` prefetches and displays the resource. It
overrides inner `<source>` tags if present

What shouldn't be working (yet):
--------------------
* The `media` attribute is not yet supported in either the PreloadScanner or the actual parser.
* The `srcset` attribute is not yet supported in either the PreloadScanner or the actual parser.

