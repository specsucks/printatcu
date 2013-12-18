NOT Print@CU
========
NOT Print@CU allows anyone to send documents to Columbia University's NINJa printing system.

Setup
-----
You will need MySQL and Redis to be installed before you can start working with the server.

    $ bundle install
    $ rails server
  
Then just point your browser at ```http://localhost:3000```
  
JK we don't give bitchass instructions.  here's how to really get started

Actually Informative Setup 
----- 

You will need ruby on rails, mysql, and redis installed, along with all 
the other libraries that will be requested when you run bundle install 
which i'm too lazy to list here.  Like libxml.  You need that one.  But 
that's not the only one you need, so don't complain when bundle install 
inevitably fails on the first few tries.

So the first step is to run 
	$bundle install 

When you get that working, you want to set up the mysql databases.  
First, copy config/databases.yml.template to config/databases.yml and 
edit in the root password for your mysql server.  You also need to 
create two databases printatcu_development and printatcu_test.  Then run

    $rake db:migrate

to populate the mysql databases.

You also need to create an account on Filepicker.io, and put the API key 
in config/initializers/filepicker.rb.  You also need to add the filepicker secret in a new file .env in the base 
directory with the line

    FILEPICKER_SECRET=

To start the application, you need to run

    $foreman run rails server

and visit
    localhost:3000

in your browser
Credits
-------
* [Sam Aarons](http://samaarons.com)
* [The Cloaked Mask](http://specsucks.wordpress.com)  

External Links
--------------
* [Print@CU](https://printatcu.com)
* [NINJa Status](http://www.columbia.edu/acis/facilities/printers/ninja_status.html)
* [NINJa Printer Locations](http://www.columbia.edu/acis/facilities/printers/locations.html)
* [Specsucks offical blog](http://specsucks.wordpress.com)
* [Specsucks official twitter](http://twitter.com/spec_sucks) 

p.s. this is NOT printatcu plz don't sue us.
