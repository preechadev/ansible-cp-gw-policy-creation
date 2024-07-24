# ansible-cp-gw-policy-creation
ansible-cp-gw-policy-creation

ansible-galaxy collection install check_point.mgmt
ansible-galaxy collection install check_point.gaia

Here is the example of the /etc/ansible/hosts file

ubuntu@ip-10-11-1-177:~$ cat /etc/ansible/hosts <br>
[check_point] <br>
<SMS_IP> <br>
#%CHECK_POINT_MANAGEMENT_SERVER_IP% <br>
[check_point:vars] <br>
ansible_httpapi_use_ssl=True <br>
ansible_httpapi_validate_certs=False <br>
ansible_user=admin <br>
ansible_password=<password> <br>
ansible_network_os=check_point.mgmt.checkpoint <br>
 <br>

Usage: 

> ansible-playbook simple-gw-policy-yml --check <br>
> ansible-playbook simple-gw-policy-yml
