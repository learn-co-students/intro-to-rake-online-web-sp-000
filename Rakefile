namespace :greeting do 
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  
  task :hola do 
    puts "hola de Rake!"
  end
end

task :environment do 
  require_relative "./config/environment.rb"
end

desc "Opens a Pry console"
task :console => :environment do
  Pry.start
end

namespace :db do
  desc "Creates student table in the database"
  task :migrate => :environment do
    Student.create_table
  end 
  
  desc "seeds db with dummy data from seed file"
  task :seed do
    require_relative "./db/seeds.rb"
  end
end

