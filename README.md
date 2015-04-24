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

- __apt__ used to install packages on debian based system.
- __yum__ the RHEL equivelent to the above
- __template__ used to pre-fill a template based on variables, then send the resulting file to the node

Once you have a playbook written, ansible parses it and does your will on the target machine through ssh.

# Let's give it a try

The first thing you need to do is [install Ansible.](http://docs.ansible.com/intro_installation.html)
Once you have it on your computer, the first thing you might want to try is running and _ad hoc_ command. 
This is the quicket way to see Ansible in action because you don't actually have to write a playbook. 

You do it like this `ansible <hosts> -m <module> -a "arguments"`

For example, if we wanted to use an ad hoc command to update a specific package we'd do it like this:
`ansible -i hosts zone1-loadbalancers -u root -m apt -a "name=openssl update_cache=yes state=latest"`

While this is indeed awesome, it barely scratches the surface of what Ansible can do! Let's clone this repo and run the provided playbook on a virtual machine to see more of it's power. 

I use DigitalOcean for quick VM's to test playbooks on. You can get a $10 credit by clicking [here](https://www.digitalocean.com/?refcode=2b1b2cf6c56b).
