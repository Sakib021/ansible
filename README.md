# ansible

#to upload codes from server
	vi README.md
	git diff README.md
	git status
	git add README.md
	git commit -m "updated readme file, initial commit"
	git push origin main

#install ansible in centos
	sudo yum install epel-release
	sudo yum install ansible


# Inventory configure and update it to the Git
	vi inventory
	git status
	git add inventory
	git status
	git commit -m "first version of inventory"
	git push origin main


# Check the server by ping 
	ansible all --key-file ~/.ssh/id_ed25519/ -i inventory -m ping


# ansible.cfg file create and uplod to the git 
	vi ansible.cfg
	ansible all -m ping
	ansible all -m gather_facts --limit 192.168.1.154
	git status
	git add ansible.cfg
	git status
	git commit -m "first config file for ansable.cfg"
	git push origin main
