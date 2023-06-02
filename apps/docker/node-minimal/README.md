# Minimal Node App Dockerfied

A minimal Node.js app that runs inside a docker container and
* Always returns "Hello World"
* Respects using Ctrl+C to exit

To build the app run<br/>
`docker build -t node-minimal .`<br/>
which will build the app (docker build, not compile anything), and give it the name "node-minimal". You can open Docker Desktop to easily see the image.

To run the app run<br/>
`docker run -p 3000:3000 node-minimal`<br/>
which will run the app by name and map local port 3000 to its internal port 3000. 

This will start a container based off of the image "node-minimal", and give it a unique name. To make things a little cleaner you can give the running container a name using --name, and automatically remove the container upon its exist using --rm.<br/>`docker run --rm --name some-name -p 3000:3000 node-minimal`

NOTE: This app will say it's running on IP 0.0.0.0 which means any network interface. You'll need to visit the app at localhost, 127.0.0.1, your public IP, etc. on the port listed.