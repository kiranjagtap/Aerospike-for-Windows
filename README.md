# Aerospike-for-Windows
This will help you how to install and run Aerospike on windows machine
install vagrant from https://www.vagrantup.com/downloads.html
install virtualbox for windows

mkdir aerospike-vm
cd aerospike-vm

vagrant init aerospike/aerospike-ce

vagrant up

--------------vagrant command-----------------------------
vagran up -> this will start virtual machine
vagran ssh -> this will log inside linux virtual box
	     ]]'
]\where aerospike is runnning and you can use tool such as aql, asadm etc.

-------------------------------------------

sudo service aerospike status
sudo service aerospike start


sudo service amc start


ip addr | grep 'global eth1'
inet 172.28.128.3/24 brd 172.28.128.255 scope global eth1


copy 172.28.128.3:8081 and paste in to browser
one popup will launch mention hotstname = localhost and click ok, this will launch Aerospike AMC console




aql->

insert into test.testset (pk,name) values('Kiran','Jagtap')
set output json
table