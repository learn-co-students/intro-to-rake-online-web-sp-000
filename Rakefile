desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :greeting do
  task :hello do
    puts "hello from Rake!"
  end
  task :hola do
    puts "hola de Rake!"
  end
end

task :console do

end

task :environment do
  require_relative './config/environment.rb'
end

namespace :db do
  desc 'create students table'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'execute file'
  task :seed => :environment do
    require_relative './db/seeds.rb'
  end
end
