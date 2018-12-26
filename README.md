# SDN-based-IaaS-Hypervisor-Overlay-solution
Implemented SDN based solution to provide on demand Infrastructure as a service for multi tenant cloud environment(VPC) using VXLAN and GRE overlay tunneling. Provided features like dynamic configuration, addition, deletion, migration of network and containers based on tenant requirement across cloud environment. Automated infrastructure creation, control plane and data plane management using python and ansible scripts.

The Controller VM's (CVM) for all the Tenants will be on a single controller Hypervisor
(which is 192.168.124.5 for this milestone)

A Tenant needs to login to his particular tenant controller vm
(for this milestone the ip of the controller vm is 172.16.<tenantid>.2)

Go to /root/ms-2/etc Directory

Edit the 'resolv.json' file, where you can specify the username, password and ip of the hypervisor's where you need to create
VM's and networks

We are providing multiple options to provide input and create the infrastructure,


Option 1(User manually editing the json): 

Edit the 'userinput.json' file, where you can specify the Tenant ID, Hypervisor ID, Subnet and Count of VM's need to be created
on that network

Run the 'run.py' Python file


Option 2(User selecting options from command Line):

Run 'createinfrastructure.py' Python file

User will be prompted with multiple options, which the user can select depending on his requirement

Note: At a single point of time an user can either add/delete/migrate his/her infrastructure on multiple hypervisors. To perform another action, the user needs to run this python file again.
      Command prompts for inputs were given in a user understandable manner


Option 3(API):

Curl post request with specified parameters should be hitting the port 5000 on local hypervisor
