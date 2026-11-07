# bcnfs.org site
Our site uses [Jekyll](https://jekyllrb.com/) and [Bootstrap](http://getbootstrap.com/).

## Development

We use [bundler](https://bundler.io/) to manage the dependencies. First, install it with `gem install bundler`.

Now, navigate to this folder and install Jekyll and the other deps with `bundle install`.

Run the development server with `bundle exec jekyll serve`.

## Internationalization

The default language is English (`en`), using the existing URLs. Catalan (`ca`)
pages live under `/ca/`. This works with GitHub Pages without custom plugins.

Each translated page has explicit `lang`, `translation_key`, and `permalink`
front matter. Versions of the same page share a `translation_key`. The language selector and
alternate-language metadata discover matching pages automatically.
Pages available in only one language keep their original URL and declare their
actual language. The selector only appears when multiple translations exist.

Shared interface strings, descriptions, home URLs, and date formats are in
`_data/locales.yml`. Page content is translated in separate files, preserving
Markdown and HTML editing. Keep internal links within the same language when a
translation exists, and use Jekyll's `relative_url` filter for links and assets.

To add a language, add its entry to `_data/locales.yml`, copy the pages into its
language directory, and set their front matter. To add a translated page, copy
its source and retain the same `translation_key` with the new language and URL.

Build with `bundle exec jekyll build`, then check `/` and `/ca/`, the language selector, internal links,
and the HTML `lang` and `hreflang` attributes.
