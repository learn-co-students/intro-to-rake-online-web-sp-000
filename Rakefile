namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'drop into pry console'
task :console do 
  Pry.start 
end

namespace :db do 

  task :environment do
    require_relative './config/environment'
  end

  desc 'migrate changes to your DB'
  task :migrate => :environment do 
    Student.create_table 
  end

  desc 'seed the DB with dummy data'
  task :seed do 
    require_relative './db/seeds.rb'
  end
end

