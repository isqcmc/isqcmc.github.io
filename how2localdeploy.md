how2localdeploy.txt

The isqcmc.org website is deployed to the web as a "mostly vanilla" github pages, using its own jekyll parser of `.md` files.
Testing changes to this website without pushing them live, on production or a "live fork", can be quite tricky.

The official point of help online is [this page](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll), but it doesn't explain everything - namely that one needs to create a local unsynced file to be able to set this up.

- create a `Gemfile` file on the root folder with:
  - ```
source "https://rubygems.org/"
gem "github-pages", "~> 228", group: :jekyll_plugins
```
- install dependencies with `bundle install`
- deploy with `bundle exec jekyll serve`


Notes:
- On Mac you may have `homebrew` with `ruby-install` and [`chruby`](https://github.com/postmodern/chruby) to be able to have different ruby versions.
- If you need to install new ruby versions use: `ruby-install ruby X.Y.Z` with version from [this page](https://www.ruby-lang.org/en/downloads/releases/)