desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hello to the terminal, in Spanish'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
  desc 'seeds the database with dummy data'
  task :seed do
    require_relative './db/seeds'
  end
end

task :environment do
  require_relative "./config/environment"
end

desc 'drop into pry console for debugging'
task :console => :environment do
  Pry.start
end
