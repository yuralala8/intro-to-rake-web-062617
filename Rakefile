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

desc 'giving our Student.create_table task access to the config/environment.rb file'
task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'creates task dependency'
  task :migrate => :environment do
    Student.create_table
end
  desc 'seeds the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
