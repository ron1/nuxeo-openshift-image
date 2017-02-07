This is a modified Nuxeo Docker image to match the security requirements of OpenShift v3.

To create a new application in OpenShift from this use:
```
$oc new-app https://github.com/nuxeo/nuxeo-openshift-image.git 
``` 

Or to pass some custom env variables ( see docker-entrypoint.sh for what you can do) 
```
$oc new-app https://github.com/nuxeo/nuxeo-openshift-image.git  
-e NUXEO_TEMPLATES=default,mongodb
-e NUXEO_CUSTOM_PARAM=nuxeo.mongodb.server=mongodb://admin:nuxeo@mongodb:27017
-e NUXEO_PACKAGES=nuxeo-web-ui
```

## About Nuxeo

Nuxeo provides a modular, extensible Java-based
[open source software platform for enterprise content management](http://www.nuxeo.com/en/products/ep),
and packaged applications for [document management](http://www.nuxeo.com/en/products/document-management),
[digital asset management](http://www.nuxeo.com/en/products/dam) and
[case management](http://www.nuxeo.com/en/products/case-management).

Designed by developers for developers, the Nuxeo platform offers a modern
architecture, a powerful plug-in model and extensive packaging
capabilities for building content applications.

More information on: <http://www.nuxeo.com/>
