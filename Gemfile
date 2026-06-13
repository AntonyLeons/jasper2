if Gem.win_platform?
  begin
    require 'ruby_installer/runtime'
    RubyInstaller::Runtime.add_dll_directory(RubyInstaller::Runtime.msys2_installation.mingw_bin_path)
  rescue StandardError
    # Ignore if MSYS2 is not installed or raises an error
  end
end

source "https://rubygems.org"


gem 'jekyll', '~> 4.4'
group :jekyll_plugins do
  gem 'jekyll-paginate'
  gem 'jekyll-feed'
  gem 'jekyll-sitemap'
  gem 'jekyll-algolia'
end

gem 'jekyll-sass-converter'
gem 'ostruct'
