## Troubleshooting
### VM installation process with vagrant / ansible
- check this out when you have trouble with ansible module for postgresql (LibraryError)
⋅⋅⋅ Handle the LibraryError exception in postgresql_db.py file as a workaround
[ansible.module_utils.postgres issue](https://github.com/ansible/ansible/issues/65223)
[workaround for the issue](https://github.com/ansible/ansible/pull/65229/files)
```
lib/ansible/modules/database/postgresql/postgresql_db.py
```
- show network connections in Ubuntu with netstat
```
sudo netstat -tunlp
```
- check Ubuntu firewall rules to allow access to postgresql database on your host system
```
sudo ufw allow from 192.168.33.101 to any port 5432
```
- use gem bindfs in vagrant to sync guest folder with proper user rights
[gem bindfs github](https://github.com/gael-ian/vagrant-bindfs)
