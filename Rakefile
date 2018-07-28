task :enviroment do
  require_relative "./config/environment"
end

namespace :greeting do
  desc "outputs hello to the terminal"
  task :hello do
    puts "hello"
  end

  desc "outputs hola to the terminal"
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc "migrate changes to your database"
  task :migrate => :enviroment do
    Student.create_table
  end

  desc "seed the database with some dummy data"
  task :seed do
    require_relative "./db/seeds.rb"
  end
end

desc "drop into the Pry console"
task :console => :enviroment do
  pry.start
end
