# Difference git pull and git fetch

* git pull brings the changes from remote repo to local repo and apply changes
* git fetch bring ths changes from remote repo and keeps it in local repo. git merge origin/branch_name to apply changes
 
# How to clone a single branch from remote repository

* git clone --single-branch -b <branch_name> <repo_url>

# what happens in background for mvn install command?

* Built-in lifecyles are: Default, Clean and Site
* Phases of default Lifecyle: Validate, Compile, Test, Verify, Package, Install and Deploy
* When running mvn install, maven will download the packages on to the local repo .m2 directory

# Settings needed before running mvn deploy command?

* Update the settings.xml in .m2 directory with Nexus repo credentials
* Update the pom.xml with nexus repo snapshots and release urls within distribution management block

# Why Maven takes much time for 1st execution and lower time for 2nd execution?

* Dependencies will be cached in local repo /.m2/ directory for the first time running mvn clean install and further use of command will refer the dependency from local repo rather than remote central repo.

# How to get present working folder ?

* command: basename "$PWD" or;
* pwd | rev | cut -d '/' -f 1 | rev

# How to copy files from local windows machine to cloud based linux machine?

* Use pscp command to transfer files
* Utilize windows powershell utility to execute the command
* pscp <filename> user@ipaddress:/path/to/paste/

# Why we need ansible ad-hoc commands?

* It is useful to execute shell modules or copy modules and target specific hosts

# How to get detailed log reports while executing ansible playbook?

* use the -vvvv parameter to get detailed logs
* ansible-playbook -i hosts demo.yaml -vvvv

# What is the purpose of ansible.cfg file?

* Present by default under /etc/ansible and useful to define certain settings in ansible.cfg

# What are the modules used and which module is used to get the file from node to master?

* Some of the common modules are Copy, Fetch, Yum, Apt, Debug, Get_url, Expect, Template, File, Command, Shell
* Use Fetch module to copy files from node to master

# An ansible playbook which has 5 tasks, 2 should run on local machine and 3 on remote node. How to execute?

* Use multiple play concept to declare different host group to execute plays.

# How to save only last 5 build jobs in jenkins job?

* Update the log rotation to 5, which make sure the last 5 builds are saved in jenkins/jobs/builds folder

# Any three best practices of docker?

* When using Dockerfile, run docker build with only necessary files as it will keep the build context size to minimum
* Use official images with proper tags as base images



