# aciansiblesandbox

> use with devnetsandbox: https://devnetsandbox.cisco.com/DevNet/catalog/aci-simulator-sandbox

On Devbox prepare env and run playbooks:

    ansible-galaxy collection install cisco.aci

create ansible.cfg with content:

    [defaults]
    interpreter_python = ~/py3venv/bin/python3



**Scenario 1 - One-Time Bulk Creation of VLANs to New or Existing Pool**

Objective:

To automate the process of creating VLANs in bulk, either by adding them to an existing pool or by creating a new pool to which these VLANs will be added.

File: 
vlan_playbook.yaml

**Scenario - Physical Interface and Policy Group Configuration for 1G, 10G, etc.**

Objective:

Automate the configuration of physical interfaces and their associated policy groups with varying speeds such as 1Gbps, 10Gbps, etc., within the Cisco ACI environment using Ansible.

File: 
interface_policy_playbook.yaml

**Scenario 3 - New Port-Channel (PC) & Virtual Port-Channel (VPC) Creation and VLAN Management**

Objective:

Automate the creation of new Port-Channels (PC) and Virtual Port-Channels (VPC), as well as the management of VLANs within these channels using Ansible, while sourcing VLAN and interface details from a common YAML file named common.yaml.

File: 
interface_config_playbook.yaml

**Scenario 4 - New Bridge Domain (BD) & Endpoint Group (EPG) Creation**

Objective:

Automate the configuration of new Bridge Domains (BDs) and Endpoint Groups (EPGs) within Cisco ACI using Ansible. This includes the setup of these entities under a single VRF as well as across multiple VRFs. The details for the BDs and EPGs will be defined in a YAML file named common.yaml to facilitate the creation process.

File: 
bd_epg_playbook.yaml

**Scenario 5 - New Access Control List (ACL) & Contract Creation**

Objective:

Automate the creation of new Access Control Lists (ACLs) and Contracts, as well as the management of these policies within Cisco ACI using Ansible. Leverage a YAML file named common.yaml to source policy and filter details for dynamic configuration.

File: 
contract_epg_playbook.yaml
