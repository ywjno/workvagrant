require 'rubygems'

desc "vagrant up"
task :up do
  system "vagrant up"
end

desc "vagrant down"
task :down do
  system "vagrant halt"
end

desc "vagrant reload"
task :reload do
  system "vagrant reload"
end

desc "install all cookbooks"
task :install do
  system "librarian-chef install"
end

desc "update all cookbooks"
task :update do
  system "librarian-chef update"
end
