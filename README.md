md-viewer
=========

A HTML5 Markdown viewer that automatically refreshes the page as you work. This was motivated by wanting to
work on Markdown files in Vim without having to manually reload them all the time, and is similar in concept
to [Dillinger](http://dillinger.io/). Dillinger is great, but I'd prefer to work directly on my files rather
than through a github or dropbox.

md-viewer uses the Markdown.Converter class from [PageDown](https://code.google.com/p/pagedown/) to perform
Markdown to HTML conversion.

Currently this is very much in alpha and is something I hacked together in an evening. It's good enough to be
useful to me right now, so it might not move much further.

Using md-viewer
===============
To use md-viewer, simply open it in a browser (so far only tested in Chrome), open your Markdown file in the
file picker, and start writing. As you work, your file will be automatically reloaded as HTML in the browser.

Reloading only happens when the file is saved to. This prevents constant reloading of your page, which would
prevent scrolling in overflowing block elements and inspecting some parts of the HTML. Furthermore, reloading
may be manually paused and resumed using the very crude pause/resume anchors at the top of the page - next to
the reload delay input. Speaking of which, the delay between reloads, in milliseconds, may be set at the top
of the page.

Styling is controlled by `md-viewer.css`. The default style imports `foghorn.css`, which has been gratefully
stolen from [jasonm23](https://github.com/jasonm23/markdown-css-themes), and adds a few modifications.

License
=======
md-viewer is available under the [MIT license](http://opensource.org/licenses/mit-license.php), the same as
PageDown/Mardown.Converter.
