# ACIT4640 - Lab 7

- A README.md file that contains: 
    - required command(s) to: 
      - create new keys
      - run included scripts to import and delete keys
      - terraform commands (init, fmt, validate, plan and apply)
      - ansible commands (syntax check, run playbook)
    - Put commands in code blocks and include a brief description of each command.
    - A screenshot of the rendered html page from one of your servers, they should be almost the same, so just a screenshot of one is fin

## Commands:
### Create new keys
```
ssh-keygen -t ed25519 -C "your_email@example.com" -f ~/.ssh/aws
```

### Run import_lab_key
```
./import_lab_key ~/.ssh/aws.pub
```

### Terraform Commands Required:
Initializes your current working directory
```
terraform init
```

Applies the terraform to create, update, or delete the infastructure
```
terraform apply
```

### Ansible Commands Required:
Check if hosts are reachable
```
ansible all -m ping
```

Check playbook syntax
```
ansible-playbook --syntax-check playbook.yml
```

Dry Run to simulate all changes
```
ansible-playbook playbook.yml --check
```


