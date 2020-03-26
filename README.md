Simple proxy server creation using Nginx inside Docker
 1. First thing to start with is install nginx.To do this in convenient manner,install brew which is the underlying package manager that installs all those UNIX and open-source utilities you might want. It's the easiest way to install them on Mac OS X, just as it is on Linux. 
 $ install brew
 $ brew install nginx
2. Now you are ready to use nginx
  $ nginx - to start nginx
3. Now you need to create Dockerfile with necessary commands to assemble an image. In the Dockerfile,I gave command to copy configuration file from current working directory to /etc/nginx/conf.d/default.conf which is the general configuration of nginx and to configure the default virtual host as well.
4.In the configuration file,you need to set server_name where you would like see your results and location includes the results you want to see.

Command to build image:  docker build . -t myapplication

Command to run: docker run -it --rm -p 80:80 myapplication
  
