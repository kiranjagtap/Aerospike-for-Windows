# Aerospike for Windows
This will help you how to install and run Aerospike on windows machine
1. install vagrant from https://www.vagrantup.com/downloads.html
2. install virtualbox for windows

3. mkdir aerospike-vm
4. cd aerospike-vm

5. vagrant init aerospike/aerospike-ce

6. vagrant up

Vagrant command

* vagran up -> this will start virtual machine
* vagran ssh -> this will log inside linux virtual box where aerospike is runnning and you can use tool such as aql, asadm etc.

Check Aerospike status and start using below commands

   1. sudo service aerospike status
   2. sudo service aerospike start

Start Aerospike AMC console using below command

   1. sudo service amc start

IP Address for Aerospike
  * Type below command to get IP address where Aerospike is running

   1. ip addr | grep 'global eth1'
 
 inet 172.28.128.3/24 brd 172.28.128.255 scope global eth1

copy 172.28.128.3:8081 and paste in to browser
one popup will launch mention hotstname = localhost and click ok, this will launch Aerospike AMC console

aql->

* insert into test.testset (pk,name) values('Kiran','Jagtap')
* set output json
* set output table
