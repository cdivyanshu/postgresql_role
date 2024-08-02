# Contains both static and dynamic inventory you can use them as per your requirements

## To Run the Playbook
```
ansible-playbook -i <your_inventory_file> --ask-vault-pass your_playbook.yml

```

## If using static inventory

- If using static inventory which is located inside test directory you need to change (host IP and location of your pem key).
- Changes host(use postgresql) in install.yml file.
  
## If using Dynamic inventory
- Changes need to be done in ansible.cfg file
   - uncomment host_key_checking = False
   - uncomment enable_plugins = aws_ec2
   - uncomment private_key_file = /home/akshit/Downloads/sonar.pem - give location of your pem key but if you are using jenkins then don't uncomment this instead store key inside jenkins credentials.
   - uncomment remote_user = ubuntu - If you are using jenkins then don't need to uncomment this because while saving the key you will be giving name of user aswell.
