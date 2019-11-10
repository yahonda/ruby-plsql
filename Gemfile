source "http://rubygems.org"

group :development do
  gem "juwelier", "~> 2.0"
  gem "rspec_junit_formatter"
end

group :test, :development do
  gem "rake", ">= 10.0"
  gem "rspec", "~> 3.1"

  unless ENV["NO_ACTIVERECORD"]
    gem "activerecord"
    gem "activerecord-oracle_enhanced-adapter"
    gem "simplecov", ">= 0"
  end

  platforms :ruby, :mswin, :mingw do
    gem "ruby-oci8", "~> 2.1"
  end
end
