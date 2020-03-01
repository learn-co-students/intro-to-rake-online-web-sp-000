desc 'outputs hello to the terminal'

namespace :greeting do
	task :hello do
	  puts "hello from Rake!"
	end

	task :hola do
		puts 'hola de Rake!'		
	end
end

task :environment do
	require './config/environment.rb'	
end

task console: :environment do
	# require 'pry'
  Pry.start
end

namespace :db do
	task migrate: :environment do
	  puts "it doesn't matter"
	end

	task :seed do
		require './lib/seed.rb'
	end

end