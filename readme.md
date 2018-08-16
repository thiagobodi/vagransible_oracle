#vagransible_oracle\
## a way to automate virtualbox hosts running oracle databases using ansible as a configuration manager tool (rather than bash)
Thiago Bodi - 16/08/2018: repository and Vagrantfile created

## Instance setup to be deployed:\
Linux distro: oracle enterprise linux 6.9\
Oracle database: 11.2.0.4 (to be obtained from oracle support patch 13390677, files 1 and 2)\
No ASM\
Single Instace\

##Pre requisites:
Download patch 13390677 from oracle support (https://support.oracle.com)\
Install vagrant (https://www.vagrantup.com/downloads.html)\
Install ansible:\
    for windows powershell: https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html\
    for cygwin http://www.oznetnerd.com/installing-ansible-windows/\
