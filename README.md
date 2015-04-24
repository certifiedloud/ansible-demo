# Ansible-demo

**DO NOT use this playbook for anything except as a demo.**

The Ansible playbook contained in this repo sets up a LAMP stack and deploys wordpress to it. 

# What is configuration management?

- In the professional world you never manage a single computer. Operations professionals are tasked with maintaining fleets of servers, workstations and
any number of other systems. You need something to help you manage the multitude of computers you must manage. Enter configuration management tools. 
There are a number of tools available:
	
	- Ansible (My favorite)
	- Puppet
	- Salt
	- Chef

I don't care which one you choose, but if you want to be a systems administrator, **you must choose one**.

# Why Ansible?

- Ansible is one of the most in-demand skills sought by employers.
According to [this random website](http://media.dice.com/report/april-2015-fastest-trending-skills/), it is the 3rd fastest growing in demand. 

- Ansible is 'agentless'. This is what sets it apart from the other tools mentioned above. You don't have to install any client software on the nodes
you wish to manage. It just uses ssh as the client. 

- Ansible is easier to use than some of the older solutions, like puppet. I've tried both, and I wouldn't even want to set up puppet without Ansible.
That's when I made up my mind about ansibele. 

# How does it work?

To make use of Ansible, you must write what's called a 'playbook'. This is nothing more than a [yaml](http://docs.ansible.com/YAMLSyntax.html) formatted file. 
You envoke any number Ansible's extensive [list of modules](http://docs.ansible.com/modules_by_category.html). 
The list of available modules is a long one, but some of the most common ones are:

	- apt used to install packages on debian based system.
	- yum the RHEL equivelent to the above
	- template used to pre-fill a template based on variables, then send the resulting file to the node

Once you have a playbook written, ansible parses it and does your will on the target machine through ssh.
