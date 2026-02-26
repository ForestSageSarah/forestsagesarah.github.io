# frozen_string_literal: true

source "https://rubygems.org"

gem "jekyll-remote-theme", "~> 0.5"
gem "jekyll-paginate", "~> 1.1"
gem "jekyll-feed", "~> 0.17"
gem "jekyll-seo-tag", "~> 2.8"
gem "jekyll-sitemap", "~> 1.4"
gem "jekyll-archives", "~> 2.2"

group :test do
  gem "html-proofer", "~> 3.18"
end

install_if -> { RUBY_PLATFORM =~ %r!mingw|mswin|java! } do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", :install_if => RUBY_PLATFORM =~ %r!mswin|mingw|cygwin!
gem "webrick", "~> 1.7"
