# About

This is the public documentation for the api-wow RESTful web service provided as part of the World of Warcraft community site.

# Documentation

Latest documentation can be found here: http://blizzard.github.com/api-wow-docs/

# Generating

Open your command line within the cloned repositories folder, and execute the follow commands. The libxml2 and libxslt libraries are required.

    $ make

This will create index-new.html that contains the built documentation.

The two commands used in the makefile are:

    $ xmllint --xinclude docbook.xml > docbook-new.xml
    $ xsltproc --stringparam html.stylesheet style.css api-wow.xsl docbook-new.xml > index-new.html
