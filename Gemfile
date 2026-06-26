source "https://rubygems.org"

# GitHub Pages builds the site with this gem, which pins Jekyll and all
# safe-listed plugins to the exact versions GitHub runs in production.
# Local preview:  bundle install  &&  bundle exec jekyll serve
gem "github-pages", group: :jekyll_plugins

# Plugins (also declared in _config.yml so GitHub Pages activates them).
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
end

# Windows and JRuby do not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance booster for watching directories on Windows.
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock http_parser.rb to v0.6.x on JRuby builds.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
