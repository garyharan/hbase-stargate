require 'rspec/core/rake_task'

begin
  require 'jeweler'

  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "hbase-stargate"
    gemspec.authors = ['Openplaces']
    gemspec.email = 'greg.lu@gmail.com'
    gemspec.homepage = "http://github.com/greglu/hbase-stargate"
    gemspec.summary = "Ruby client for HBase's Stargate web service"
    gemspec.description = "A Ruby client used to interact with HBase through its Stargate web service front-end"
    gemspec.files = FileList["{lib,spec}/**/*","Rakefile","VERSION","LICENSE","README.textile"].to_a
    gemspec.extra_rdoc_files = FileList["LICENSE","README.textile"].to_a

    gemspec.add_development_dependency "rspec"
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler not available. Install it with: sudo gem install jeweler"
end

RSpec::Core::RakeTask.new do |t|
  t.rspec_opts = ["-c", "-f progress", "-r ./spec/spec_helper.rb"]
  t.pattern = 'spec/**/*_spec.rb'
end
