# ansible-ucs
UCS Playbook samples and Modules for Ansible using UCSMSDK

### Dependencies

Download and install the UCS Python SDK:

https://communities.cisco.com/docs/DOC-64378

### UCS Ansible Slack Chat
Feel free to join chat for questions or enhancement requests:

http://tiny.cc/ucsm-slack

## Emulate UCS Manager
You can visit https://communities.cisco.com/docs/DOC-37827 for more information on how to have a virtual UCS Manager for testing this project as well before issuing it to your production.

### Usage
* Update library/inventory file with UCSM login info.  
* Run the command and include where the full location where you put ansible-ucs repo: export PYTHONPATH="${PYTHONPATH}:/ansible-ucs"

### To run a playbook:
ansible-playbook site.yml or run them from the plays/dir or create your own

PLAY [ucs] *********************************************************************

TASK [Login X.X.X.X] *****************************************************
ok: [ucspe]

TASK [Configure Callhome X.X.X.X] ****************************************
changed: [ucspe]

TASK [Logout X.X.X.X] ****************************************************
ok: [ucspe]

PLAY [ucs] *********************************************************************

TASK [Login X.X.X.X] *****************************************************
ok: [ucspe]

TASK [Configure SNMP X.X.X.X] ********************************************
changed: [ucspe]

TASK [Logout X.X.X.X] ****************************************************
ok: [ucspe]

PLAY RECAP *********************************************************************
ucspe                      : ok=6    changed=2    unreachable=0    failed=0

### Current Playbooks/Supported Modules
* configuring of callhome
* disabling of callhome
* enabling/disabling snmp
* adding snmp traps
* adding VSAN's
* adding VLAN's
* adding DNS Server IP
* removing DNS Server IP
* adding NTP server
* remove NTP server

### Playbooks/Modules Coming Soon
Uplink Configuration
Interface Configuration
vNic Template Creation
