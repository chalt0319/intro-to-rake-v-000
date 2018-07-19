desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc 'outputs hello from Other to the terminal'
task :hi do
  puts "hello from the Other Rake!"
end

namespace :db do

  desc 'requires environment'
  task :environment do
    require_relative './config/environment'
  end

  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

  desc 'drop into the Pry console'
  task :console => :environment do
    Pry.start
  end

end
