task :default => :tests

desc "Run Server"
  task :rackup do
	sh "rackup"
  end
  
desc "run the chat server"
task :server do
  sh "bundle exec ruby chat.rb"
end  
  
  
desc "Test (default)" 
  task :tests => :spec do
	sh "ruby test/test.rb"
  end

desc "make a non Ajax request via curl"
task :noajax do
  sh "curl -v http://localhost:4567/update"
end

desc "make an Ajax request via curl"
task :ajax do
  sh %q{curl -v -H "X-Requested-With: XMLHttpRequest" localhost:4567/update}
end

desc "Visit the GitHub repo page"
task :open do
  sh "open https://github.com/Michelle9/SYTW_P6.git"
end

desc "Run tests in local machine"
task :local_tests do
   sh "gnome-terminal -x sh -c 'rackup' && sh -c 'ruby test/test.rb local'"
end

desc "Open repository"
task :repo do
  sh "gnome-open https://github.com/Michelle9/SYTW_P6.git"
end

desc "run specs"
task :spec do
  sh "bundle exec rspec spec/spec.rb"
end