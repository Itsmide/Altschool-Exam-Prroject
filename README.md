# ALTschool-Exam-Project

Created by https://github.com/Itsmide

URL: https://itsmidealtschoolexamproject.live/ (IP in hosts)

Perquisites for running this ansible-playbook on your remote machine

1. Make sure your machine is up to date 
   using "sudo apt update && sudo apt upgrade -y"

2. you need to configure mySQL. this has to be done manually. Using
   -  sudo wget https://dev.mysql.com/get/mysql-apt-config_0.8.22-1_all.deb
   - sudo apt install ./mysql-apt-config_0.8.22-1_all.deb

     Before Running Playbook

1. Edit the 'host-inventory' file for your remote IP address
  
2. Must edit 'ubuntu20' file for root {{mysql_pass}}

3. Must configure your git user.name and email in 'web-apt-installation.yml'

4. Must change SQL database and users to desired name in 'database-setup.yml'

5.  Should edit the .env not in the 'database-setup.yml', to your IP address, Root_SQL Details.

6. Should edit the laravel.conf to your IP address in 'database-setup.yml'

               Order of Running Playbook

-  web-apt-installation
-  set_root_pass_ubuntu20.yaml
-  database-setup.yml
-  last-setup.yml 

Also, bash script for installation of POSTGRESQL are added to last-setup.yml, which will run togther in the ansible-playbook.

 
Created by https://github.com/Itsmide
URL: https://itsmidealtschoolexamproject.live/ (IP in hosts)
