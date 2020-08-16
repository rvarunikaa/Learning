# Learning
learning technologies

Error on windows 10 home edition when using docker for windows
Permission denied issues when creating a docker container. - Fix needs adding your current user to the docker group

whoami => this wil give user name (sayy this is XXX)
Soln: 
New-LocalGroup -Name 'docker-users' -Description 'docker Users Group'
Add-LocalGroupMember -Group 'Administrators' -Member ('docker-users') –Verbose 
Add-LocalGroupMember -Group 'docker-users' -Member ('xxx','Administrators') –Verbose
