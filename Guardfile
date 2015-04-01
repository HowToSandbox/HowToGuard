# Guard for rake and bundler

## Uncomment and set this to only include directories you want to watch
  # directories %w(spec)

## Uncomment to clear the screen before every task
 clearing :on





# Guard autowatches itself and exits upon change.
# Put the following in your rake file
# Then run 'rake guard' to start guard
    #task :guard do
      # puts "INFO: Starting GUARD in loop mode."
      # sleep (1)
      # system 'while bundle exec guard; do echo "Restarting Guard..."; done'
      # Guard internally checks for changes in the Guardfile.
      # This task restarts Guard when changes are detected.
    #end

# bundler
    guard :bundler, cmd: "bundle" do
      watch('Gemfile')
      watch(%r{^Gemfile$})
    end



# Rake
  #test
    guard 'rake', :task => 'test:run_all', :run_on_start => false, :run_on_all => false do
      watch(%r{^spec/test/.+$})
      watch(%r{^support/.+$})
      watch(%r{^require\.rb$})
      #this watches /spec/test, /support, and require.rb
    end
  #sandbox
    guard 'rake', :task => 'sandbox:run_all', :run_on_start => false, :run_on_all => true do
      watch(%r{^spec/sandbox/.+$})
      watch(%r{^support/.+$})
      watch(%r{^require\.rb$})
    end