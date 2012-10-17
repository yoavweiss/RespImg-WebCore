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


