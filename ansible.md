```
ansible-galaxy install -r roles/requirements.yml -p roles/
ansible-playbook myplaybook.yaml -i myinventory -e ansible_password=$MYPASS -e ansible_user=$MYUSER
```