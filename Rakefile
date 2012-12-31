require 'rubygems'

desc "vagrant up"
task :up do
  system "vagrant up"
end

desc "vagrant halt"
task :down do
  system "vagrant halt"
end

desc "vagrant reload"
task :reload do
  system "vagrant reload"
end

desc "install all cookbook"
task :install_cookbook do
  system "librarian-chef install"
end

desc "update all cookbook"
task :update_cookbook do
  system "librarian-chef update"
end
