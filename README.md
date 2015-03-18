# GooglePirateExtended
Google Pirate Extended v4 is an extension for the browser that will enhance the experience on Google by adding some new and useful features.
Use Google to find free music, tv shows, movies, anime, torrents, comics, books and other files stored publicly online.

## Contribute
You can contribute to Google Pirate Extended v4 by different means. You can help find bugs (and report them in the [issue tracker](https://github.com/teocci/GooglePirateExtended/issues).

### Optional requirements
To build the Chrome extension it is required to be able to run executable, which can be done in Wine on Linux or on a Windows computer.

It is possible to build the unpacked version of the Chrome or Maxthon extension without the need to run executables:
 * `ant copy-chrome` -- Makes the required files to build the extension file (.crx) ready in the build directory.

### Signing
The certificates for signing the extensions have to be provided by yourself and have to be placed in:
 * `/.cert/chrome/`
 
It should be noted that the Ant build will create a new signing key for Chrome if it's missing from `/.cert/chrome/` (Running executables is required).
 
### Ant
The build system is made in Ant and requires both Ant and Java to be installed.

 * `ant all` -- Build everything below except for the styles.
 * `ant devnumber` -- Increment the build number.
 * `ant firefox` -- Build the Firefox addon (.xpi)
 * `ant chrome` -- Build the Chrome extension (.crx)
 * `ant userscript` -- Build the userscript (.user.js)

### Build Properties (build.properties)
The keys in this file have the prefix and suffix `@`.

 * `devbuild` -- Set to true if you want to create a developer build and false if it's a stable release.
 * `ant-version` -- The stable version.
 * `ant-revision` -- The stable revision used to check if it's a newer version.
 * `pastebin-api-key` -- The pastebin API key used by Google Pirate Extended v4 to post the debug log on pastebin.
 * `name-stable` -- The name of the extensions for the stable version.
 * `name-dev` -- The name of the extensions for the developer version.
 * `stable-downloadURL` -- The location of the newest version of Google Pirate Extended v4 for the stable version.
 * `stable-updateURL` -- The location of the userscript header to check if a new version of Google Pirate Extended v4 is available for the stable version.
 * `dev-downloadURL` -- The location of the newest version of Google Pirate Extended v4 for the developer version.
 * `dev-updateURL` -- The location of the userscript header to check if a new version of Google Pirate Extended v4 is available for the developer version.
 * `firefox-target-id` -- Used in the Firefox extension manifest to specify which platform the extension is targeted towards.
 * `firefox-target-min-version` -- The minimum version of the targeted platform.
 * `firefox-target-max-version` -- The maximum version of the targeted platform.
 * `firefox-update-link` -- The location of the newest version of the developer version of Google Pirate Extended v4 for Firefox is located.
 * `firefox-update-rdf` -- The location of the file, which Firefox uses to check if a new version of the developer version of Google Pirate Extended v4 is available.
 * `chrome-id` -- The id of the Chrome extension. The id can be found in `chrome://extensions/` or calculated from the signing key.
 * `chrome-update-xml` -- The location of the file, which Chrome uses to check if a new version of the developer version of Google Pirate Extended v4 is available.
 * `chrome-update-file` -- The location of the newest version of the developer version of Google Pirate Extended v4 for Chrome is located.

## License
The MIT License (MIT)

Copyright (c) 2015 Jorge Frisancho

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
