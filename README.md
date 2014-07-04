This is the main OHC Website

### Changes

Development environment as a vagrant VM available [here](https://github.com/openhealthcare/developer)

    $ vagrant ssh
    $ cd /usr/lib/ohc/static-ohc
    $ rvm use 1.9.3@ohcstatic
    $ jekyll serve -w

Source code will be mounted to the host at developer/src/static-ohc
