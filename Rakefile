namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
  puts "hello from Rake!"
  end

  desc 'outputs hello to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'set up environment'
  task :environment do
    require_relative './config/environment'
  end

  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'add dummy data to database'
  task :seed do
    require_relative './db/seeds'
  end

  desc 'open Pry console'
  task :console => :environment do
    Pry.start
  end
end
