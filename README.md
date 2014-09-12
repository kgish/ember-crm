# ember-crm

This is an example CRM application using ember.js and taken from [Vic Ramon's Ember Tutorial](http://ember.vicramon.com/).

## Installation

In order to install this on your own system you will have do to the following:

    $ git clone git@github.com:kgish/ember-crm.git 
    $ cd ember-crm
    $ rvm use 2.1.0@ember-crm --create
    $ rvm --rvmrc ruby-2.1.0ember-crm
    $ rvm rvmrc trust `pwd`
    $ rvm rvmrc warning ignore `pwd`/.rvmrc
    $ bundle install
    $ rake db:create

## Secret

You will also need to create the secrets file. To generate the secret token run the following command:

    $ rake secret
    2ad688adc10...dab4c
    
Create the secrets file using the secret token generated above:

    $ cat config/secrets.yml
    development:
        secret_key_base: 2ad688adc10...dab4c
 
    test:
        secret_key_base: 2ad688adc10...dab4c
 
    production:
        secret_key_base: <%= ENV["SECRET_KEY_BASE"] %>

You should now be able to run the applications by running the following command:

    $ rails s
    
