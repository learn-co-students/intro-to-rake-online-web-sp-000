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


task :environment do 
  require_relative './config/environment'
end


namespace :db do


desc 'migrate changes to your database. it depends on the environment task to load up the environment.rb file'
task :migrate => :environment do 
    Student.create_table
end


desc 'seed: to populate some dummy data. the dummata data is stored in seeds.rb. the file contains ruby code to create student instnaces in ruby (not sql). u dont need extra loading because the seeds.rb itself alreayd required the student.rb file to create the student classes. all youre doing now is load the seeds.rb file'
task :seed do
  require_relative './db/seeds.rb'
end

end 




desc 'console: its just a prying tool using file. what u pry depends on what u load. here i load the environment.rb file thru the :environment task, which has access to the student.rb file and the students.db database... that means i can interact with the database (create stuff, et stuff) as well as create intances of students... kinda like having a bin/run file to play with.. testing things out... really nice. instead of typing stuff to the run file and run the file i can do "irb" style... very nice'
  task :console => :environment do
    Pry.start
  end