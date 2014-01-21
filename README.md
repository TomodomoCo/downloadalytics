# Downloadalytics
A free PHP script for tracking file downloads in Google Analytics

If you're not PHP/Apache-savvy, [**Van Patten Media**](http://www.vanpattenmedia.com/) can install the script for you, for $200 per standard installation. [Get in touch](http://www.vanpattenmedia.com/) to learn more.

## Installation
Downloadalytics requires some basic setup:

1. Download the [Server Side Google Analytics](https://github.com/dancameron/server-side-google-analytics) class, and make sure to update the path in `download.php`
2. Set your Google Analytics property ID and domain name
3. Replace references to `your-site.com` with the proper domain name (if your downloads are hosted on a subdomain, you should also update the reference to `www` in the script)
4. Replace the `mp3` filetype with the type you want to track.

At this point, you're ready to go! URLs will be formatted as `http://your-site.com/download.php?url=http://your-site.com/path/to/download.mp3`.

You can also optionally set up the included `.htaccess` rewrite directives, to clean up the URLs.

The `.htaccess` rewrite assumes a few WordPress-y things:
*   It assumes your files are stored in a `wp-content/uploads` folder
*   It assumes your files are in year and date subfolders (the WordPress default; e.g. `your-site.com/wp-content/uploads/2014/01/file.mp3`)

The `.htaccess` will rewrite URLs formatted as `http://your-site.com/download/2014/01/file.mp3` to `http://your-site.com/download.php?url=http://your-site.com/wp-content/uploads/2014/01/file.mp3`. This is easy to modify with basic regex/rewrite experience.

## MIT License
Copyright © Van Patten Media Inc., <http://www.vanpattenmedia.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
