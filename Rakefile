desc 'outputs hello to the terminal'
namespace :greeting do
  task :hello do
    puts "hello from Rake!"
  end
  
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end

namespace :db do
  task :environment do
    require_relative './config/environment'
  end
  
  task :migrate => :environment do
    Student.create_table
  end
  
  task :seed => :environment do
    Student.create(name: "Melissa", grade: "10th")
    Student.create(name: "April", grade: "10th")
    Student.create(name: "Luke", grade: "9th")
    Student.create(name: "Devon", grade: "11th")
    Student.create(name: "Sarah", grade: "10th")
  end
end