# Ansible-EC2
How to deploy EC2 in AWS and terminate the machines using Ansible.
This project assumes that you already have the credential file configured

```
vi ~/.aws/config

```

If do not have it, then you can do so by using 

```
aws configure
```

To use this start_ec2.yml playbook, I am also assuming that the following services pre-exists in the AWS account 

1. Key pair
2. VPC
3. Security group
4. Subnet

To terminate running EC2 instance, you can simply use the play book terminate.yml. The play uses prompt variable, which means after running the playbook, you need to provide the instance id of the running EC2 machines. 

Before running the playbooks make sure you change the **vars.yml** file 

How to run Ansible playbooks

```
ansible-playbook <playbook.yml>
```


