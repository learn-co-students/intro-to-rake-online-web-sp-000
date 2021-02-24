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

namespace :db do
  desc 'migrate changes to the database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'load sample data into the database'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'load the necessary files and gems'
task :environment do
  require_relative './config/environment'
end

desc 'open Pry'
task :console => :environment do
  Pry.start
end