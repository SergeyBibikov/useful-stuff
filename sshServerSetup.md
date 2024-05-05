# update the system
	sudo apt-get update && sudo apt-get upgrage -y && sudo apt-get autoremove -y

# install openssh-server
	sudo apt install openssh-server
	sudo systemctl restart ssh

# check that 22 port is open
	sudo lsof -i -P -n | grep LISTEN

# check the ufw status and open ssh port if it's active
	sudo ufw status
	if active: sudo ufw allow 22

# connect to the machine
	ssh {user}@{IP address | hostname}
	accept the fingerprint and type the password
