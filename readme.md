# Apply configuration using ansible to cisco devices
Deploy configuration to cisco devices.

**NOTE**: This script is functional in any UNIX system such Ubuntu, WSL, it might work in MacOS.

# Pre-Requisites
You must have Python3(version 3.6.8 or higher), pip3 and Ansible installed(version 2.9.13 or higher). Once is done, clone this repository

# Install ansible dependencies

1. On WSL ubuntu or Linux server copy the .ini, .yml and .txt files
2. The .ini file will need to be updated with the IPs/host address and credentials used for accessing the devices
3. The .txt files are base on configuring a Lo0 interface in three different devices
3. On the .yml file you will need to update some variables according to your .ini file
3. Install the ansible cisco.ios.ios_config module using `ansible-galaxy collection install cisco.ios`
4. Disable the host key checking `export ANSIBLE_HOST_KEY_CHECKING=False`

# Running the script
Use the next command to run the playbook:

`ansible-playbook ansible-output-commmands.yml -i inventory.ini`
