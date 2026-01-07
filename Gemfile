source 'https://rubygems.org'
git_source(:github) { |repo| "https://github.com/#{repo}.git" }

ruby '>= 3.1'

# Bundle edge Rails instead: gem 'rails', github: 'rails/rails'
gem 'rails', '~> 7.1.0'

# Moved above coverband so I can debug coverband during rails startup
group :development, :test do
  # Call 'byebug' anywhere in the code to stop execution and get a debugger console
  gem 'pry-byebug', platforms: [:mri]
end

# gem 'pg', platforms: [:mri]
gem 'sqlite3', '~> 1.4'

# Use Puma as the app server
gem 'puma'

# Asset pipeline
gem 'sprockets-rails'
gem 'cssbundling-rails'
gem 'jsbundling-rails'

gem 'material_icons'

# Turbo and Stimulus (Rails 7 defaults)
gem 'turbo-rails'
gem 'stimulus-rails'

# Build JSON APIs with ease
gem 'jbuilder'

# When explaining observability
gem 'newrelic_rpm'
gem 'sentry-ruby'
gem 'sentry-rails'

# exploring dumping all lines
gem 'binding_dumper'

# Reduces boot times through caching; required in config/boot.rb
gem 'bootsnap', require: false

gem 'sidekiq'

group :development do
  gem 'listen'
  gem 'rubocop'
end

group :test do
  gem 'capybara'
  gem 'selenium-webdriver'
  gem 'minitest-ci'
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:windows, :jruby]
gem 'nokogiri'

# Coverband for production code coverage
gem 'coverband'
