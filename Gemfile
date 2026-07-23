source "https://rubygems.org"

group :development do
  gem "rspec_junit_formatter"
  gem "rdoc"

  platforms :jruby do
    gem "rbs", ">= 4.1.0.pre.2" # Use the java-platform gem so JRuby does not build the C extension
  end
end

group :rubocop do
  gem "rubocop", require: false
  gem "rubocop-performance", require: false
  gem "rubocop-rails", require: false
end

group :test, :development do
  gem "rake", ">= 10.0"
  gem "rspec", "~> 3.1"
  gem "logger"

  unless ENV["NO_ACTIVERECORD"]
    gem "activerecord", github: "rails/rails", branch: "main"
    gem "activerecord-oracle_enhanced-adapter", github: "rsim/oracle-enhanced", branch: "master"
    gem "simplecov", ">= 0"
  end

  platforms :ruby, :windows do
    gem "ruby-oci8", "~> 2.1"
  end
end
