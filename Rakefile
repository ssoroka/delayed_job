require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name     = "delayed_job"
    gem.version  = "1.7.0"
    gem.date     = "2008-11-28"
    gem.summary  = "Database-backed asynchronous priority queue system -- Extracted from Shopify"
    gem.email    = "tobi@leetsoft.com"
    gem.homepage = "http://github.com/tobi/delayed_job/tree/master"
    gem.description = "Delated_job (or DJ) encapsulates the common pattern of asynchronously executing longer tasks in the background. It is a direct extraction from Shopify where the job table is responsible for a multitude of core tasks."
    gem.authors  = ["Tobias Lütke"]
    gem.has_rdoc = false
    gem.rdoc_options = ["--main", "README.textile"]
    gem.extra_rdoc_files = ["README.textile"]

    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end

rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require 'spec/rake/spectask'
Spec::Rake::SpecTask.new(:spec) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.spec_files = FileList['spec/**/*_spec.rb']
end

Spec::Rake::SpecTask.new(:rcov) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rcov = true
end


task :default => :spec
