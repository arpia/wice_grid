require 'rake'
require 'rake/testtask'
require 'rdoc/task'

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the wice_grid plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the wice_grid plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'WiceGrid'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README.rdoc')
  rdoc.rdoc_files.include('SAVED_QUERIES_HOWTO.rdoc')
  rdoc.rdoc_files.include('RELEASE_NOTES_3.2.pre1.rdoc')
  rdoc.rdoc_files.include('CHANGELOG')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

begin
  require 'git'
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "wice_grid"
    gem.summary = %Q{Rails Grid Plugin}
    gem.description = %Q{A Rails grid plugin to create grids with sorting, pagination, and (automatically generated) filters }
    gem.email = "yuri.leikind@gmail.com"
    gem.homepage = "http://github.com/hikki--/wice_grid"
    gem.authors = ["Yuri Leikind"]
    gem.add_dependency "kaminari", ">= 0.13.0"
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

