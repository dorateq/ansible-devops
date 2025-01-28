##### Running your Playbook
CMD : ansible-playbook docker/docker-install.yml -l srv-01 -u ansible --ask-become-pass -k

# The fLAGS 
-l flag specifies your server and the 
-u flag specifies which user to log into on the remote server, 
-k is for passing SSH password on command line.
--ask-become-pass Specifies password for "sudo" activities
