# KASM

Streaming containerized apps and desktops to end-users.
The Workspaces platform provides enterprise-class orchestration,
data loss prevention, and web streaming technology to enable 
the delivery of containerized workloads to your browser.

It is done using kASM vnc which is open sources

## Install KASM

#### Swap file

Creat swap partition.

	sudo dd if=/dev/zero bs=1M count=1024 of=/mnt/1GiB.swap

Upgrade the permision

	sudo chmod 600 /mnt/1GiB.swap

Enter the swap partition

	sudo mkswap /mnt/1GiB.swap

Turn on swap partion

	sudo swapon /mnt/1GiB.swap

Verify swap

	cat /proc/swapsAdd swap to fstab

Add swap to fstab

	echo '/mnt/1GiB.swap swap swap defaults 0 0' | sudo tee -a /etc/fstab


#### Install KASM

Download KASM

	wget https://kasm-static-content.s3.amazonaws.com/kasm_release_1.10.0.238225.tar.gz

unzip the file

	tar-xf kasm_release*.tar.gz

start the setup script

	sudo baxh kasm_release/install.sh

### Get into KASM

Type in your ip addres in browser where you can login via one
of the id given to you like show in the secret file.
From there you can stream tools such as vs code, gimp, TOR, ubuntu 
via your browser from an dicker container
