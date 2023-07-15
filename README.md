# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions







Rvm 3.0.0
Installed rails 7.0.1
Rails new spree_task
Cd spree_task
gem 'spree' # core and API
gem 'spree_backend' # Rails admin panel (optional)
gem 'spree_emails' # transactional emails (optional)
gem 'spree_sample' # dummy data like products, taxons, etc
gem 'spree_auth_devise', '~> 4.3' # Devise integration (optional)
gem 'spree_gateway', '~> 3.9' # payment gateways eg. Stripe, Braintree (optional)
gem 'spree_i18n', '~> 5.0' # translation files (optional) 
 
# only needed for MacOS and Ruby 3.0
gem 'sassc', github: 'sass/sassc-ruby', branch: 'master'


 bundle install

bin/rails g spree:install --user_class=Spree::User
bin/rails g spree:auth:install
bin/rails g spree_gateway:install
bin/rails javascript:install:esbuild
bin/rails g spree:backend:install

bin/rake railties:install:migrations
bin/rails db:migrate
bin/rails db:seed
bin/rake spree_sample:load
* ...
