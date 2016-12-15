### Start project
```bash
# run
vagrant up
# provision
vagrant provision
```
Visit http://192.168.100.100/

### Ansible resources
* [Tutorial](http://docs.ansible.com/ansible/quickstart.html)
* [YAML syntax](http://docs.ansible.com/ansible/YAMLSyntax.html)
* [Glossary](http://docs.ansible.com/ansible/glossary.html)
* [Modules](http://docs.ansible.com/ansible/modules_by_category.html)
* [Documentation](http://docs.ansible.com/)
* [GitHub examples](https://github.com/ansible/ansible-examples)

### Useful commands
```
# Install from roles
ansible-galaxy install -r requirements.yml -p roles
# Install role
ansible-galaxy install geerlingguy.nginx
# Check syntax
ansible-playbook playbook.yml --syntax-check
# Run playbook
ansible-playbook -i /path/to/inventory playbook.yml -u ssh_user --key-file=/path/to/ssh-key
# Run playbook on listed hosts
ansible-playbook -i "localhost," playbook.yml
# Run ad-hoc command on localhost
ansible all -i "localhost," -c local -m shell -a 'echo hello world'
```
