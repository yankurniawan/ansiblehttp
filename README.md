ansiblehttp
===========

A python script to trigger ansible run in AWS VPC using http request.

You need to install cherrypy first:

`pip install cherrypy`  

Update the server configuration in the script:

`'server.socket_host':` *private_ip_address_of_your_ansible_instance*  
`'server.socket_port': 7780`  

`# chmod +x ansiblehttp`  
`# ./ansiblehttp`  

From the new instance run:

`curl http://ansibleipaddress:7780/ansible?playbook=something.yml`

