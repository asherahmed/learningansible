# learningansible


This playbook was created using ansible on Amazon Linux 2. To setup MariaDB 10.3 and Wagtail. Please make sure the following:
  - Playbook is tested and deployed on Ubuntu 10.04 Bionic LTS
  - Make sure the machine is not auto updating apt if you want to run update_ubuntu role
  - If Ubuntu is auto updating, please remove the lock file or kill the processes and restart machine.
# Steps:
  - Install ansible
  - Replace the roles folder in your own ansible directory
  - Run playbook-wagtail with argument -K to give sudo password
  - Use sudo mysql to test MariaDB
  - Go to port 8000 for Wagtail CMS
# Features!

  - It will install MariaDB 10.3 without creating a root user.
  - The wagtail is served with uWsgi and Nginx acting as a reverse proxy on server.
  - Supervisor is used to run uWsgi as a service in emperor mode.
  - Default superuser for Wagtail is admin: ansible123
