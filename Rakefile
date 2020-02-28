
namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc "outputs hola to the terminal"
  task :hola do
    puts "hola de Rake!"
  end
end

desc "load in the environment"
task :environment do
  require_relative "./config/environment"
end

desc "drop into the Pry console"
task :console => :environment do 
  Pry.start
end

namespace :db do
  desc "migrate chanes to the DB"
  task :migrate => :environment do
    Student.create_table
  end

  desc "seed the DB with values"
  task :seed => :environment do
    require_relative "./db/seeds"
  end
end