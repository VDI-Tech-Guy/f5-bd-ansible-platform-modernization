# F5 BIG-IP Modernization through Automation Collection

## Description

This  repository delivers a turnkey Ansible automation framework aimed at modernizing legacy F5 BIG-IP platforms by streamlining the migration, upgrade, and restoration of critical configurations across older and newer appliance models. The codebase is organized into distinct folders for standalone (single-node) and high-availability (HA) deployments, and includes a comprehensive roles directory encapsulating reusable functionality such as backup (UCS/crypto), disable tasks, tenant creation, and restoration workflows.

Organizations running older BIG-IP hardware or software versions often face challenges when upgrading to newer F5 platforms such as **rSeries**, **VELOS**. Manual migration and restoration processes are error-prone and time-consuming, especially in **high-availability (HA)** environments.  

## Ansible playbooks and roles

We provide Playbooks and Roles for F5 BIG-IP Modernization through Automation, which can be implemented using Ansible Automation Platform Controller. There are at examples in each scenario (standalone, HA) containing example variables and provided recommended group_vars and host_var names. Additionally, demonstration videos of the solutions in use are provided at the bottom.

## Purpose of this collection

This code is intended for customer/partner use and the primary intent of this codebase is to provide a repeatable, automated solution for migrating and upgrading from Legacy F5 BIG-IP platforms (iSeries, non-iSeries, Viprion, VCMP) to Next-Gen BIG-IP Platforms (rSeries/Velos) in enterprise environments.

## Requirements

- Python 3.11 or later
- `ansible-core` 2.15 or later

- Users also need to include platform collections as per their requirements. The supported platform collections are:
  - [f5networks.f5_bigip](https://github.com/F5Networks/f5-ansible-bigip)
  - [f5networks.f5_modules](https://github.com/F5Networks/f5-ansible)
  - [f5networks.f5os](https://github.com/F5Networks/f5-ansible-f5os)

## Execution environment

- If you would like to utilize an existing Execution Environment in your Lab for this EE its located at 
  - [F5 Ansible Execution Engine Link](https://quay.io/f5_business_development/f5_ee_new)

## Supported topologies

- **Standalone BIG-IP systems** — single appliance or virtual instance.
- **High-Availability pairs** — supporting both combined and sequential upgrade paths.

## Installation

To consume this Validated Content from Automation Hub, please ensure that you add the following lines to your ansible.cfg file.

```
[galaxy]
server_list = automation_hub

[galaxy_server.automation_hub]
url=https://cloud.redhat.com/api/automation-hub/
auth_url=https://sso.redhat.com/auth/realms/redhat-external/protocol/openid-connect/token
token=<SuperSecretToken>
```
The token can be obtained from the [Automation Hub Web UI](https://console.redhat.com/ansible/automation-hub/token).

Once the above steps are done, you can run the following command to install the collection.

```
ansible-galaxy collection install 
```

## Use case

Once installed, you can reference the f5-bd-ansible-platform-modernization collection content to import Templates into Ansible Automation Platform Controller to migrate from older F5 BIG-IP platforms to newer ones.

## Example execution context

- Executed from **Ansible Automation Platform** against F5 devices using `httpapi` or `local` connections.
- Playbooks and README files are located under:
  - `standalone/`
  - `high_availability/`
- Commonly used to migrate from Legacy **BIG-IP 15.x or 16.x** Versions to **BIG-IP 17.x or 21.x**, or to transition from legacy hardware to modern F5 platforms like **rSeries** and **VELOS**.

## YouTube demonstration

If you want to see an example of the code in use, before it became a verified collection, watch [this video](https://www.youtube.com/watch?v=V676EF_bq-4).

## Support

As a validated collection, you can get support through Ansible Automation Platform (AAP) using the **Create issue** button on the top right corner.
If a support case cannot be opened with Red Hat and the collection has been obtained either from Galaxy or GitHub, there may community help available on the [Ansible Forum](https://forum.ansible.com/).

## License

GNU General Public License v3.0 or later

See [LICENSE](https://github.com/f5devcentral/f5-bd-ansible-platform-modernization/blob/main/LICENSE) to see the full text.
