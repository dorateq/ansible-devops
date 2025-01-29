##### Examples for Running your Playbook
CMD 1 : srv-01 requires password SSH connection
  ansible-playbook docker/docker-install.yml -l srv-01 -u ansible --ask-become-pass -k

CMD 2: srv-02 requires pki connection.
  ansible all -m ping  --private-key "~/.ssh/oracle_oci.key"

CMD 3: Connect to both srv-01 and srv-02 with pki and password
ansible-playbook docker/docker-install.yml -l srv  --private-key "~/.ssh/oracle_oci.key" -k

# The fLAGS 
-l flag specifies your server and the 
-u flag specifies which user to log into on the remote server, 
-k is for passing SSH password on command line.
--ask-become-pass Specifies password for "sudo" activities
