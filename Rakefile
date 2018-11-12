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
  desc 'setup environment'
  task :environment do
    require_relative './config/environment.rb'
  end

  desc 'migrate database by applying sql that changes it'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the db with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

end
