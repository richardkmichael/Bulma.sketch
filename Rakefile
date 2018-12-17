require "pry"

task default: :monitor

task :monitor do
  dist = "./dist"
  # bulma = "#{dist}/Bulma.sketch"
  puts "Watching #{dist}"

  require "bundler"
  Bundler.setup

  require "rb-fsevent"
  fsevent = FSEvent.new
  fsevent.watch dist do |path, data|
    puts "Events: #{data.events.count}"
    # binding.pry
  end
  fsevent.run
end
