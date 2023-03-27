```
ansible-galaxy install -r roles/requirements.yml -p roles/
ansible-playbook myplaybook.yaml -i myinventory -e ansible_user=$TARGET_VMUSER -e ansible_password=$TARGET_VMPASS
```
