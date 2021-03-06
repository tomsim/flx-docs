Getting ready with opxflexswitch 
==========================================

::
    
    Prerequisites - Preinstalled Docker on the host machine.



Please use below script to set up docker containers that can be
used to experiment with opxflexswitch.

:: 
    
    To run the script 

    sh docker_startup.sh

The script sets up the docker environment. 

1) It creates 2 docker containers d_inst1 and d_inst2 .

2) eth25 is created on d_inst1 and eth35 is created on d_inst2

Here is the detailed explanation for each step in the script  

docker pull 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This command will pull the latest image from docker hub.
   
 
:: 
  
   Snaproute opxflexswitch image is added in the docker hub 
   https://hub.docker.com/r/snapos/flex/
   
   docker hub has 2 tags for images
  
   auto - This is the default ubuntu image with packages installed that are needed for opxflexswitch. 
          Such as redis , syslog. This DOES NOT have opxflexswitch installed on it.
   Flexv<version_number> - Latest opxflexswitch image for docker. This image tag will be used for all   
                           the tutorials next.

   Example - 
   docker pull snapos/flex:Flexv46
   


Starting the container 
^^^^^^^^^^^^^^^^^^^^^^^^^
- Instantiate docker container with different flags

docker run -dt --privileged --log-driver=syslog --cap-add=ALL  --name d_inst1   -P libero18/ubuntu-14.04:flex1


::

 **Note**  The flags used while spawning container . Which are necessary for proper functioning of the opxflexswitch
    --log-driver  This will enable syslog support for logging
    --cap-add=ALL In order to create/get on  linux interfaces enable all permissions.
   

Verify Flexswitch installation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- When docker container is spawned by default we start rsyslogd and redis-server. 


- /etc/init.d/opxflexswitch is the script to start /stop the opxflexswitch daemons. 

:: 

 
/etc/init.d/opxflexswitch <start/stop/restart>

Basic commands 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- Start opxflexswitch 

::

    service opxflexswitch start



- To access all REST APIs use swagger 

http://localhost:8080/api-docs/

- Check system health 

::
 
    http://<host_ip>:8080/public/v1/state/SystemStatus

    {
    "ObjectId": "",
    "Object": {
    "ConfigObj": null,
    "Name": "7abb27f0ad2a",
    "SwVersion": "",
    "Ready": true,
    "Reason": "None",
    "UpTime": "19h54m58.355328307s",
    "NumCreateCalls": "Total 19 Success 15",
    "NumDeleteCalls": "Total 0 Success 0", 
    "NumUpdateCalls": "Total 4 Success 4",
    "NumGetCalls": "Total 1 Success 0",
    "NumActionCalls": "Total 0 Success 0",
    "FlexDaemons": [
    {

- In case you need to flush all database and restart all daemons

::

   redis-cli
    run command "flushdb"


- Note that the successive tutorials will cover detailed illustrations about configuration and debugging.
