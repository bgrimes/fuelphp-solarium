# Description

This [Fuel PHP](http://fuelphp.com/) package will add [Solarium](http://www.solarium-project.org/) to your application. 

# To Install

In the root of your fuel application run 

    git submodule add git://github.com/bgrimes/fuelphp-solarium.git fuel/packages/solarium

# To Use

This wrapper loads the [Solarium](http://www.solarium-project.org/) library into your project so that you can either autoload the package
in your config file or load it on the fly

    // Load the config from app/config/solr.php
    \Config::load("solarium", true); 
    \Package::load('solarium');

The config file can be used to store connection information, but your can of course tweak it to suit your
needs for dealing with Solarium.

After the package is loaded you can use it as defined on the [Solarium](http://www.solarium-project.org/) website, for example:

    
    $config = \Config::get("solarium.solr_app.adapteroptions");

    // Create a client instance
    $client = new \Solarium_Client($config);

    ...


