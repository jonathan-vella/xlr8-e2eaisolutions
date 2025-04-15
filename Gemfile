source 'https://rubygems.org'

gem "github-pages", "~> 232", group: :jekyll_plugins
gem "just-the-docs", "~> 0.10.1" # Use a version compatible with GitHub Pages
gem "minima", "~> 2.5"  # Add minima as a fallback theme
gem "csv"  # Add CSV gem to address warning
gem "faraday-retry"  # Add faraday-retry gem to address warning

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-remote-theme"
  gem "jekyll-seo-tag", "~> 2.8"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
gem "tzinfo", ">= 1", "< 3", :platforms => [:mingw, :x64_mingw, :mswin, :jruby]
gem "tzinfo-data", :platforms => [:mingw, :x64_mingw, :mswin, :jruby]

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to ~> 0.6.0 to avoid "undefined symbol: rb_str_new_cstr"
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

# webrick is no longer bundled with Ruby 3.0, add it explicitly
gem "webrick", "~> 1.8"
