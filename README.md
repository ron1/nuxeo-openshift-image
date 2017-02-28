These are sample modified Nuxeo Docker images(Debian and Centos based) to match the security requirements of OpenShift v3.
For the official supported Docker images, go to: https://github.com/nuxeo/docker-nuxeo

To create a new application in OpenShift from this use:
```
$oc new-app https://github.com/nuxeo/nuxeo-openshift-image.git --context-dir=debian 
``` 
or

```
$oc new-app https://github.com/nuxeo/nuxeo-openshift-image.git --context-dir=centos
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
