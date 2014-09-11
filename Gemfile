source 'https://rubygems.org'

gem "rails", "3.2.19"
gem "jquery-rails", "~> 2.0.2"
gem "coderay", "~> 1.1.0"
gem "fastercsv", "~> 1.5.0", :platforms => [:mri_18, :mingw_18, :jruby]
gem "builder", ">= 3.0.4"
gem "request_store", "1.0.5"
gem "mime-types"
gem "rbpdf", "~> 1.18.0"

# Optional gem for LDAP authentication
group :ldap do
  gem "net-ldap", "~> 0.3.1"
end

# Optional gem for OpenID authentication
group :openid do
  gem "ruby-openid", "~> 2.3.0", :require => "openid"
  gem "rack-openid"
end

platforms :mri, :mingw do
  # Optional gem for exporting the gantt to a PNG file, not supported with jruby
  group :rmagick do
    # RMagick 2 supports ruby 1.9
    # RMagick 1 would be fine for ruby 1.8 but Bundler does not support
    # different requirements for the same gem on different platforms
    gem "rmagick", ">= 2.0.0"
  end

  # Optional Markdown support, not for JRuby
  group :markdown do
    # TODO: upgrade to redcarpet 3.x when ruby1.8 support is dropped
    gem "redcarpet", "~> 2.3.0"
  end
end

gem "mysql2", "~> 0.3.11"

group :development do
  gem "rdoc", ">= 2.4.2"
  gem "capistrano", '2.5.15'
  gem "yard"
end

group :test do
  gem "shoulda", "~> 3.3.2"
  gem "mocha", "~> 1.0.0", :require => 'mocha/api'
  gem "capybara", "~> 2.1.0"
  gem "selenium-webdriver"
end

gem 'unicorn'
