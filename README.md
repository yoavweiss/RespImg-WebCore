The Responsive Images WebCore fork!!!
--------------------

This repository contains experiments in adding the `<picture>` element to
WebKit's WebCore library.

It is based on Chromium's WebKit from 17/10/12.

Build instructions:
----------------------
* Build Chromium like you normally would on [Linux](http://code.google.com/p/chromium/wiki/LinuxBuildInstructions) or [OSX] (http://code.google.com/p/chromium/wiki/MacBuildInstructions)
* If your time is precious, use [Ninja](http://code.google.com/p/chromium/wiki/NinjaBuild)
* Download the patch from [here](https://raw.github.com/yoavweiss/RespImg-WebCore/master/picture_patch.txt) to your /tmp directory
* Apply the patch using `(cd third_party/WebKit/Source/WebCore && patch -p0 < /tmp/picture_patch.txt)`

Binaries:
--------------------------
* Ubuntu 64 binary can be found [here]( https://github.com/downloads/yoavweiss/RespImg-WebCore/chrome.7z)
* OSX binary can be found [here]( https://github.com/downloads/yoavweiss/RespImg-WebCore/Chromium.app.tar.gz)

Test page:
---------------------
Once you got your new binary, you can see `<picture>` in action [here] (http://yoavweiss.github.com/RespImg-WebCore/)
*Note:* Currently only `<picture src>` is displaying. `<picture><source src></picture>` is preloaded, but not displayed.
*Note #2:* `<picture src>` is not supposed to work in the final implementation, since `<img>` can do that just fine
