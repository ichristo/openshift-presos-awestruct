How to run Awestruct Presentation Hostin on OpenShift
======================================================

This will give you an empty PHP setup on OpenShift for hosting your presentations on an Awestruct site.

Installation
------------

Create OpenShift application

    rhc app create -a presos -t php-5.3 --from-code git://github.com/openshift-presos-awestruct.git
<<<<<<< HEAD

now build your presentation using Awestruct. Once done, copy the _site directory to your OpenShift instance.

    cp -rv  $project/_site presos/php

To deploy to OpenShift just commit and push

    git add presos/php/*

=======

now build your presentation using Awestruct. Once done, copy the _site directory to your OpenShift instance.

    cp -rv  $project/_site presos/php

To deploy to OpenShift just commit and push

    git add presos/php/*

>>>>>>> bf0c78b9191867d275ef0aaef2ea0fd714b55fb5
    git co -a

    git push origin master

If you add an index.html file with the links to each presentation you have installed on the site, then you can find them here

    http://presos-$namespace.rhcloud.com

What is this project doing?
---------------------------

* Install awestruct if not available (ruby gems)
* Update awestruct when already available (ruby gems)
* Generate the site to static files

<<<<<<< HEAD
=======
Releases
--------

- v0.1 - initial setup.
>>>>>>> bf0c78b9191867d275ef0aaef2ea0fd714b55fb5
