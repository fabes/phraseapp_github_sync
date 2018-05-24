source 'https://rubygems.org'

ruby '2.0.0'

git_source(:github) do |repo_name|
  repo_name = "#{repo_name}/#{repo_name}" unless repo_name.include?('/')
  "https://github.com/#{repo_name}.git"
end

# Bundle edge Rails instead: gem 'rails', github: 'rails/rails'
gem 'rails', '~> 4.2.4'

# Database
gem 'sqlite3'

# background worker and mailer
gem 'sidekiq', '~> 3.4.2'
gem 'sinatra', '>= 1.3.0', require: nil # sidekiq monitor

# cron jons
gem 'whenever', '~> 0.9.4', require: false

# for uploading images to s3 via the froala wysiwg editor
gem 'aws-sdk', '~> 2.2', '>= 2.2.30'
gem 'wysiwyg-rails', '~> 2.8', '>= 2.8.1'

# Use the slim templating system
gem 'slim-rails', '~> 3.0.1'

# View dependencies
gem 'will_paginate', '~> 3.1'
gem 'csv_builder', '~> 2.1.1'
gem 'actionview-encoded_mail_to', '~> 1.0.4'
gem 'wicked_pdf', '~> 1.0', '>= 1.0.5'
gem 'wkhtmltopdf-binary', github: 'pallymore/wkhtmltopdf-binary-edge', tag: 'v0.12.2'

# I18n gems
gem 'rails-i18n', '~> 4.0.4'
gem 'money-rails', '~> 1.6'
gem 'money-open-exchange-rates', '~> 0.7.0'
gem 'country_select', '~> 3.0'

# Session authentication
gem 'authlogic', '~> 3.4.2'

# API
gem 'bcrypt'                # authentication
gem 'jbuilder', '~> 2.0.7'  # Read more: https://github.com/rails/jbuilder

# payment gateways
gem 'stripe', ['>= 1.31.0', '< 1.42']
gem 'plaid', '~> 1.7', '>= 1.7.1'
gem 'oauth2', '~> 0.8.0'

# Validation
gem 'valid_email', '~> 0.0.4', :require => 'valid_email/email_validator'

# Asset Pipeline
gem 'sass-rails', '4.0.3'       # Use SCSS for stylesheets
gem 'compass', '0.12.2'
gem 'compass-rails', '2.0.0'
gem 'uglifier', '>= 1.3.0'      # Compressor for JavaScript assets
gem 'coffee-rails', '~> 4.0.1'  # .js.coffee assets and views

# Assets dependencies
gem 'gon', '~> 5.2', '>= 5.2.3'
gem 'jquery-rails', '~> 3.1.0'
gem 'foundation-rails', '5.2.3.0'
gem 'foundation-icons-sass-rails'
gem 'font-awesome-rails', '~> 4.7'
gem 'ngmin-rails' #Angular
gem 'momentjs-rails', '~> 2.17', '>= 2.17.1'
gem 'filepicker-rails', '~> 1.0.0'
gem 'recaptcha', '~> 0.4.0', require: 'recaptcha/rails'

gem 'unicorn', '~> 5.2'

# Blog integration
# rack-reverse-proxy helps put a 3rd party blog in a sub dir.
# https://medium.com/@parterburn/wordpress-inside-a-ruby-on-rails-app-c324fbf39ad8
gem 'rack-reverse-proxy', :require => 'rack/reverse_proxy'

# for throttling abusive requests and ban IPs
gem 'rack-attack', '~> 4.3.0'
gem 'rack-mini-profiler', require: false

# External Services
gem 'koala', '~> 1.10.0'            # Facebook graph api and tab operations
gem 'restforce', '~> 2.1.0'         # Salesforce Integration
gem 'mailchimp_api_v3', '~> 0.1.0'
gem 'appsignal'                     # error notifications
gem 'geoip', '~> 1.6.3'             # get country by ip
gem 'useragent', '~> 0.16.8'        # parse user agent
gem 'rgb', '~> 0.1.0'

group :doc do
  # bundle exec rake doc:rails generates the API under doc/api.
  gem 'sdoc', require: false
end

#### Testing suite https://mattbrictson.com/minitest-and-rails
group :development, :test do
  gem 'dotenv-rails', '~> 2.0.2'
  gem 'better_errors'
  gem 'binding_of_caller'
  gem 'pry-byebug'
  gem 'awesome_print'
  gem 'terminal-notifier'
  gem 'terminal-notifier-guard', :require => false

  # Add spec DSL support (describe/let/it) to Minitest
  gem 'minitest-rails'
end

group :development do
  # Guard for running tests automatically upon file save
  gem 'guard', '>= 2.2.2', :require => false
  gem 'guard-minitest', :require => false
  gem 'rb-fsevent', :require => false
  gem 'letter_opener'
  gem 'quiet_assets'
end

group :test do
  gem 'launchy'
  gem 'minitest-reporters'
  gem 'webmock'
  gem 'vcr'
  gem 'fakeredis', require: 'fakeredis/minitest'
  gem 'simplecov'
end

group :production do
  gem 'redis-rails'
end

gem 'turbolinks', '~> 2.5', '>= 2.5.4'