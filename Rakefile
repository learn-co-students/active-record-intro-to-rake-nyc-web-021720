namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hello in spanish to the terminal'
  task :hola do 
    puts "hola de Rake!"
  end
end

desc 'drop into the Pry console'
task :console do 
  Pry.start 
end

namespace :db do 
  desc 'provides access to environment.rb'
  task :environment do
    require_relative './config/environment'
  end

  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds database with dummy data'
  task :seed do 
    require_relative './db/seeds'
  end
end
