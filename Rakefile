# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "hotseat"
  gem.homepage = "http://github.com/eladkehat/hotseat"
  gem.license = "MIT"
  gem.summary = %Q{Add work queue functionality to an existing CouchDB database}
  #gem.description = %Q{longer description of the gem}
  gem.email = "eladkehat@gmail.com"
  gem.authors = ["Elad Kehat"]
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

task :default => :spec

require 'yard'
YARD::Rake::YardocTask.new
