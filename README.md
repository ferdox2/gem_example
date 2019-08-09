# HOW TO CREATE A RUBY GEM

In this little text I am going to explain how to create a Ruby Gem using Bundler.


## Pre-requisites

 - For this example you need to have installed Bundler. If you do not have it just need to run the next sentence in a command prompt:
>$ gem install bundler

- Now we have all the necessary to create a Ruby gem.

## Creating a Ruby Gem using Bundler

 1. Open a command prompt and run the next sentence:
 >$bundle gem 'gem_name'
 >**NOTE:** gem_name refers to the of your Ruby gem and could it be whatever you want.
 2. In my case I use the option '-t rspec' to specify that I'm going to use RSpec as testing environment. By default Bundler assign minitest. So my sentence for this example looked like this:
 >$bundle gem gem_example -t rspec
 3. Bundler will create our gem and if It's the first time we run the command, Bundler gonna ask for accept some licence permissions, just we have to accept them.  
 4. Now you can add your code in the lib directory.
 >**NOTE:** If you add gems in the gem file, you must install them with the command: $ bundle install 

## Structure of the Ruby Gem directory
Here I'm gonna show you the structure of the gem directory and a little description of some files and directories.
```
gem_example
└───bin
│    │ console
│    │ setup
│ CODE_OF_CONDUCT.md
│ gem_example.gemspec -> The gemspec defines what’s in the gem, who made it, and the version of the gem.    
│ Gemfile -> In this file you must include all the gems that are you using in your project.
└───lib > This folder contains the files with your code.
│   └───gem_example -> In this folder you have to put your classes files 
│   │     │ version.rb -> Here you can update the version of your gem.  
│   │ gem_example.rb
│ LICENSE.txt 
│ Rakefile
│ README.md -> This file includes the information of your Ruby Gem. You can write whatever you want about your project like instructions, notes, installation process, etc.               
└───spec -> This folder contains the testing files. For each class file you must create a testing file. 
    │ gem_example_spec.rb
    │ spec_helper.rb
```
