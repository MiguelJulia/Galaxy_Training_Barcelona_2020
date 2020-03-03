# Galaxy_Training_Barcelona_2020
Usefull scripts and exercises from Galaxy Admin Training Barcelona 2020, slides here: https://github.com/galaxyproject/dagobah-training/tree/2020-barcelona


## Software support
Galaxy versions are only supported for 1y. Update is mandatory!


## Ansible
Ansible tutorial:  https://training.galaxyproject.org/training-material/topics/admin/tutorials/ansible/tutorial.html#your-first-playbook-and-first-role
Ansible Glaxy repo:  https://galaxy.ansible.com/


Ansible basic inventory structure:
.
├── group_vars
│   └── my_hosts.yml
├── hosts
├── playbook.yml
└── roles
    └── my-role
        ├── defaults
        │   └── main.yml
        ├── files
        │   └── test.txt
        ├── tasks
        │   └── main.yml
        └── templates
            └── test.ini.j2


Execute ansible playbook from inventory:
ansible-playbook -i hosts playbook.yml


Execute ansible playbook from inventory and enumerate differences:
ansible-playbook -i hosts playbook.yml --check --diff


List host metadata:
ansible -i hosts -m setup my_hosts | less


Add some roles from Ansible Galaxy:
ansible-galaxy install -p roles/ geerlingguy.git


## Install Galaxy
Install Galaxy tutorial:
https://training.galaxyproject.org/training-material/topics/admin/tutorials/ansible-galaxy/tutorial.html


## Tool management
Toolshed tools now:
* Can be installed with conda
* Are Singualrity and Docker compatible
* There are automatic importers for perl, python y R tools:   ephemeris
* Replicate other Galaxy instances by exporting and installing their tools and workflows list with ephemeris


## Biocontainers
Biocontainers surveilance and build containers in real time of many bioinformatics repositories
Galaxy is compatible with both Singularity and Docker containers
Tools from the toolshed create their own conda environment for each one individually


## User management
Users:  https://training.galaxyproject.org/training-material/topics/admin/tutorials/users-groups-quotas/slides.html#6


## Auth Methods
LDAP

