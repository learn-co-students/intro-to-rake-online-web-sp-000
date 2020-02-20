namespace :greeting do
  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end

  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
end

desc 'requires the environment for the migrate task'
task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'seeds the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

  desc 'migrates changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
end

desc 'drops into the pry console'
task :console do
  Pry.start
end
