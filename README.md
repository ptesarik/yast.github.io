yast.github.io
==============

[![CI](https://github.com/yast/yast.github.io/actions/workflows/surge.yml/badge.svg)](https://github.com/yast/yast.github.io/actions/workflows/surge.yml)
[![Documentation Status](https://readthedocs.org/projects/yastgithubio/badge/?version=latest)](https://readthedocs.org/projects/yastgithubio/?badge=latest)


Repository to host the YaST landing page (http://yast.github.io) and some
general YaST documentation.

YaST is a complex project spread over a big amount of repositories in GitHub.
The main goal of the page is to provide a clear view of the whole project at a
central point for both users and developers, but with a stronger focus in the
later.

Since the source code if spread over several repositories following an
organization that (almost always) makes sense, there is no reason to centralize
the documentation of that source code. Therefore the goal is not to offer a
central source of information, but a starting point that aggregates links
to the sources of information (whenever are they maintained by the
developers) in a way that makes sense and is easy to digest for newcomers.

Beside the files of the landing page itself, there is also a ```doc``` directory
with documentation targeted to developers and that are related to the project as
a whole and, as such, does not completely fit in any of the source code
repositories.


Updating this Documentation
---------------------------

There is an automatic spell check run for each pull request or commit. If you
want to run it locally you need to install ```aspell``` first:

    $ sudo zypper install aspell aspell-en aspell-devel

Then install the ruby bindings for aspell:

    $ bundle install --path .vendor/bundle

To run the spell checker run:

    $ bundle exec rake

### Custom Dictionary ###

File `.spell.dict` contains a custom dictionary (one word per line)
with project specific words and abbreviations. If a correct word is reported
as misspelled you can add it to the list.

*Note: The installed default English dictionary used in CI might be different than
in your system, the check may pass locally, but can fail at CI. In that case
add the missing word to the custom dictionary.*
