# ansible-cp-gw-policy-creation
ansible-cp-gw-policy-creation

Here is the example of the /etc/ansible/hosts file

ubuntu@ip-10-11-1-177:~$ cat /etc/ansible/hosts
[check_point]
<SMS_IP>
#%CHECK_POINT_MANAGEMENT_SERVER_IP%
[check_point:vars]
ansible_httpapi_use_ssl=True
ansible_httpapi_validate_certs=False
ansible_user=admin
ansible_password=<password>
ansible_network_os=check_point.mgmt.checkpoint


Usage: 

# ansible-playbook simple-gw-policy-yml --check
# ansible-playbook simple-gw-policy-yml
