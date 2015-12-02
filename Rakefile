# encoding: utf-8

require 'rake/testtask'
require 'rubocop/rake_task'

Rake::TestTask.new do |t|
  t.libs = %w( lib test )
  t.test_files = FileList['test/**/test_*.rb', 'test/**/*_spec.rb']
end

RuboCop::RakeTask.new(:rubocop) do |task|
  task.options  = %w( --display-cop-names --format simple )
  task.patterns = ['lib/**/*.rb', 'test/**/*.rb']
end

task :default => [:test, :rubocop]
