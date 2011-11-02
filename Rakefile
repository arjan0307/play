require 'rubygems'
require 'rake'

#############################################################################
#
# Standard tasks
#
#############################################################################

task :default => :test

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

desc "Open an irb session preloaded with this library"
task :console do
  sh "irb -rubygems -r ./lib/play.rb"
end

#############################################################################
#
# Custom tasks (add your own tasks here)
#
#############################################################################

$LOAD_PATH.unshift File.expand_path(File.dirname(__FILE__) + '/lib')

require 'yaml'

task :environment do
  require 'lib/play'
  require "bundler/setup"
end

desc "Open an irb session preloaded with this library"
task :console do
  sh "irb -rubygems -r ./lib/play"
end
