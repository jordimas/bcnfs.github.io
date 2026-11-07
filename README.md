# bcnfs.org site
Our site uses [Jekyll](https://jekyllrb.com/) and [Bootstrap](http://getbootstrap.com/).

## Development

We use [bundler](https://bundler.io/) to manage the dependencies. First, install it with `gem install bundler`.

Now, navigate to this folder and install Jekyll and the other deps with `bundle install`.

Run the development server with `bundle exec jekyll serve`.

## Translations

English pages keep their existing URLs; Catalan pages live under `/ca/`.
Shared strings are in `_data/locales.yml`. Translated pages declare `lang`,
share a `translation_key`, and set their own `permalink`. The language selector
links matching pages. Pages available only in Catalan keep their original URLs.

To add a translation, copy the page into its language directory and update its
front matter and internal links. No additional Jekyll plugins are required.
