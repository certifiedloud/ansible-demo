# Ansible-demo

**DO NOT use this playbook for anything except as a demo.**

The Ansible playbook contained in this repo sets up a LAMP stack and deploys wordpress to it. 

# Why Ansible?

- In the professional world you never manage a single computer. Operations professionals are tasked with maintaining fleets of servers, workstations and
any number of other systems. You need something to help you manage the multitude of computers you must manage. Enter configuration management tools. 
There are a number of tools available:
	
	- Ansible (My favorite)
	- Puppet
	- Salt
	- Chef

I don't care which one you choose, but if you want to be a systems administrator, **you must choose one**.

- Ansible is one of the most in-demand skills sought by employers.
According to [this random website](http://media.dice.com/report/april-2015-fastest-trending-skills/), it is the 3rd fastest growing in demand. 

- Ansible is 'agentless'. This is what sets it apart from the other tools mentioned above. You don't have to install any client software on the nodes
you wish to manage. It just uses ssh as the client. 
