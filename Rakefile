desc 'requires the environment file for the db tasks'
task :environment do
  require_relative './config/environment.rb'
end

namespace :greeting do
  desc "Puts 'Hello' to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "Puts 'Hola' from the terminal"
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc "Migrate changes to the database"
  task :migrate => :environment do
    Student.create_table
  end

  desc "Seed the db with some dummy data"
  task :seed do
    require_relative './db/seeds.rb'
  end

  desc "testing my own rake task"
  task :recall => :environment do
    Student.all
  end
end

desc "drop into a Pry console"
task :console => :environment do
  Pry.start
end
