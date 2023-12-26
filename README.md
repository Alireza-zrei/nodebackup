## gathering nodes backups
### Note that in this senario it only gathers SSH users backup you can change the directories later in backup.yaml

 Before starting you should install ansible 
```
apt install ansible
```

## Hosts

create your Hosts 

```
[hosts]
"domain or host IP" ansible_ssh_port="portnumber" ansible_ssh_user="username" ansible_ssh_pass="password"

```

 you can add many ip or domain like this command and save name file "hosts"

 Edit the hosts name in backup.yaml 

```
vim / nano backup.yaml
change first line : - hosts: "name set in hosts file"

```

 RUN the backup

```
ansible-playbook -i hosts(hostfile name) backup.yaml

```

 the backup files lists in the /tmp directory 
