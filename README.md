Configure localhost as a jumphost:
- `fail2ban` using firewalld [docs](https://fedoraproject.org/wiki/Fail2ban_with_FirewallD#Running_the_service) - no email alerts
- `ansible-hardening` [docs](https://docs.openstack.org/ansible-hardening/latest/index.html) - default settings

# Installation and Setup

On CentOS 8.4:

```shell
sudo yum install -y git python3
python3 -m venv venv
. venv/bin/activate
pip install -U pip
pip install -r requirements.txt
ansible-galaxy role install -r requirements.yml 
ansible-playbook site.yml
```

