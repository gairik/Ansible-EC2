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

1. key_name - Key pair
2. vpc_id - VPC
3. group_id - Security group
4. subneta - Subnet

To terminate running EC2 instance, you can simply use the play book terminate.yml. The play uses prompt variable, which means after running the playbook, you need to provide the instance id of the running EC2 machines. 


How to run Ansible playbooks

```
ansible-playbook <playbook.yml>
```


