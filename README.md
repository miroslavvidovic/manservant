# Manservant

Browse man pages in style with your personal manservant.

Fed up with browsing manual pages in a console using `less` or Googling for
the man page only to realize that your local install differs from the man page
you found? Me too, so last night I forked the original [Manservant](https://github.com/jimeh/manservant), fixed some issues and improved it to serve up
local man pages over HTTP with some pretty UI sprinkled over it.

Here's vim man page served to you by manservant:

![preview](https://imgur.com/bCvNdqe.png)

## Improvements

The original Manservant isn't maintained any more and the last update was over 5 years ago. This version tries to make Manservant more usable by fixing some issues, adding new functionality and by improving the UI.

- Manservant now works under Linux (tested on Ubuntu)
- There is an option to search for man pages from the web interface
- Sidebar has its own scroll bar (useful for man pages with many sections, e.g., bash)

## Requirements

- [Ruby][].
- [Bundler][] Ruby gem.

[ruby]: http://www.ruby-lang.org/
[bundler]: http://gembundler.com/

## Installation

Manservant is a simple [Sinatra][] application, and is run just like any other
Rack application.

[sinatra]: http://www.sinatrarb.com/

### Pow

The simplest way to run manservant is through [Pow][]. Ensure you have Pow
installed and working, and run the following to install manservant:

    git clone https://github.com/jimeh/manservant.git ~/.pow/man
    cd ~/.pow/man
    bundle install

Then visit [http://man.dev/](http://man.dev/) in your browser.

[pow]: http://pow.cx/

### Other

There's many ways to run a Rack application, and I'm not gonna cover that
here. But if you merely want to get manservant up and running to have a look,
just clone the repo and run `rackup` inside the project directory:

    git clone https://github.com/jimeh/manservant.git ~/Projects/manservant
    cd ~/Projects/manservant
    rackup

Then visit [http://localhost:9292/](http://localhost:9292/) in your browser.

## Credits

- Original version of [Manservant][] by [jimeh][],
- Man page to HTML conversion is done by [man2html][], which is bundled into
  manservant.
- The HTML UI style is shamelessly ripped from the [ronn][] gem's HTML output
  format.

[jimeh]: https://github.com/jimeh
[manservant]: https://github.com/jimeh/manservant
[man2html]: http://dcssrv1.oit.uci.edu/indiv/ehood/man2html.html
[ronn]: http://rtomayko.github.com/ronn/ronn.1.html

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License

Copyright (c) 2017 Miroslav Vidovic

MIT License

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
