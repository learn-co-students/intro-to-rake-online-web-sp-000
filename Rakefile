namespace :greeting do
  task :hello do
    desc 'outputs hello to the terminal'
    puts "hello from Rake!"
  end

  task :hola do
    desc 'outputs hola to the terminal'
    puts "hola de Rake!"
  end
end

task :environment do
  require_relative './config/environment'
end

task :console do
  desc 'drop into the Pry console'
  task :console => :enivornment do
    Pry.start
  end
end

namespace :db do
    desc 'migrate changes to your database'
    task :migrate => :environment do
      Student.create_table
    end

    desc 'seed the database with somee dummy data'
    task :seed do
      require_relative './db/seeds.rb'
    end
end