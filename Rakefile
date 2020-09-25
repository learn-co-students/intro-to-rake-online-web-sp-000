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
  desc 'migrate changes to your database'
  task :migrate => :environment do # task dependency (task :migrate dependent on task :environment)
    Student.create_table
  end

  desc 'seed the database with dummy data'
  task :seed do
    require_relative './db/seeds'
  end
end

desc 'give task access to config/environment.rb'
  task :environment do 
    require_relative "./config/environment"
  end

desc 'drop into the Pry console'
task :console => :environment do # dependent on :environment task so classes and db connection load first
  Pry.start
end
# rake -T only works if tasks have descriptions