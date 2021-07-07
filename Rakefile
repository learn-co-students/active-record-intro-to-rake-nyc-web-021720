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
  require_relative './config/environment.rb'
end
namespace :db do 
  desc "migrate changes to database"
  task :migrate  => :environment do 
      Student.create_table
  end
end
namespace :db do
  desc "seed the database with some dummy data"
  task :seed do
    require_relative "./db/seeds.rb"
  end
end
 desc " drop into the pry console" 
 task :console => :environment do 
  pry.start 
 end
