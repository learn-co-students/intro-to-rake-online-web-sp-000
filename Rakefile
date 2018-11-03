namespace :greeting do
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  task :migrate => :environment do

  end

  task :seed do
    require_relative './db/seeds.rb'
  end
end

task :environment do
  
end