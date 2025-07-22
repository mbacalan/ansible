# Ansible Setup


Local: `ansible-playbook local.yml -K --ask-vault-password`


Remote: `ansible-pull -U https://github.com/mbacalan/ansible.git -K --ask-vault-password`


### Known issues

`chsh` requires PAM authentication on Debian/Ubuntu which causes the task to fail.

Temporary solution: `sudo sed s/required/sufficient/g -i /etc/pam.d/chsh`

Reference: https://askubuntu.com/questions/812420/chsh-always-asking-a-password-and-get-pam-authentication-failure
