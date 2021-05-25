This is basic cloud native build pack flask app test

Required files:

web.py which contains flask app code
requirements.txt which containes dependency libraries
The Procfile specifies the command-line used to execute the application at runtime. In this case the Procfile declares that the web.py file contains your FLASK_APP, calls flask run, and binds the web-server to the --host with the IP address 0.0.0.0 and binds port with 8080

commands:

check pack installed : pack

pack builders suggest   ==> lists available builders

pack config default-builder builder_name   => setting up default builder

pack config default-builder  ==> Shows the current default builder

Building Image using pack:

 pack build venkat/cb-python-sample:1.0.0


Creating a docker container from image:

docker run -d -p 8080:8080 --name python-demo-app venkat/cb-python-sample:1.0.0

docker ps

curl http://localhost:8080

Removing the container:

docker stop python-demo-app

docker remove python-demo-app


Refereences:

https://tanzu.vmware.com/developer/guides/python/cnb-gs-python/
https://github.com/GoogleCloudPlatform/buildpack-samples
https://buildpacks.io/docs/tools/pack/
https://github.com/benwilcock/buildpacks-python-demo.git
