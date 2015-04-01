require 'rake/testtask'
require 'rspec'
require 'rspec/core/rake_task'


  task :guard do
    puts "INFO: Starting GUARD in loop mode."
    sleep (1)
    system 'while bundle exec guard; do echo "Restarting Guard..."; done'
    # Guard internally checks for changes in the Guardfile and restarts.
  end


namespace :test do

    RSpec::Core::RakeTask.new(:run_all) do |t|
      t.verbose = true
      t.pattern = FileList['spec/test/*.rb']
    end
end

namespace :sandbox do
  RSpec::Core::RakeTask.new(:run_all) do |t|
	t.verbose = true
	t.pattern = FileList['spec/sandbox/*.rb']
  end
end