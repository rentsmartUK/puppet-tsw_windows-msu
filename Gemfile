# vim: set ts=2 sw=2 ai et syntax=ruby:
source 'https://rubygems.org'

if ENV.key?('PUPPET_VERSION')
  puppet_version = "= #{ENV['PUPPET_VERSION']}"
else
  puppet_version = ['>= 2.7']
end

# https://github.com/jimweirich/rake
gem 'rake', '~> 12.3.3'

# https://github.com/rspec/rspec
# https://www.relishapp.com/rspec/rspec-core/v/2-0/docs
gem 'rspec'
gem 'rspec-core'
gem 'rspec-expectations'
gem 'rspec-mocks'
gem 'minitest', '~> 5.0.0'

# https://github.com/freerange/mocha#bundler
gem 'mocha', :require => false

# https://github.com/puppetlabs/puppet
gem 'puppet', puppet_version

# see http://projects.puppetlabs.com/issues/21698
platforms :mswin, :mingw do
  gem 'sys-admin', '~> 1.5.6', :require => false
  gem 'win32-api', '~> 1.4.8', :require => false
  gem 'win32-dir', '~> 0.3.7', :require => false
  gem 'win32-eventlog', '~> 0.5.3', :require => false
  gem 'win32-process', '~> 0.6.5', :require => false
  gem 'win32-security', '~> 0.1.4', :require => false
  gem 'win32-service', '~> 0.7.2', :require => false
  gem 'win32-taskscheduler', '~> 0.2.2', :require => false
  gem 'win32console', '~> 1.3.2', :require => false
  gem 'windows-api', '~> 0.4.2', :require => false
  gem 'windows-pr', '~> 1.2.1', :require => false
  gem 'minitar', '~> 0.6', :require => false
end

# https://github.com/jumanjiman/jumanjiman_spec_helper
gem 'jumanjiman_spec_helper'

gem 'ffi', '~> 1.9.3'

if File.exists? "{__FILE__}.local"
  eval(File.read("#{__FILE__}.local"), binding)
end