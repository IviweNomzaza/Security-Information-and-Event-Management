# SIEM-XDR-LAB

This is a 2-Phase project detailing the deployment and threat intelligence gathering of my local tailnet environment.
Deployment 
This phase covers deployment and baseline investigation: standing up a Wazuh manager and indexer, enrolling six agents across four operating systems over a Tailscale mesh, and validating that FIM, rootcheck, and SCA compliance scanning work end to end.

Agents and their respective roles:

wazuh-manager	Zorin OS (Linux)	000	SIEM manager, indexer, dashboard, Postfix mail relay

win-agent	Windows 11	003	Physical host + VMware hypervisor for the Linux VMs below; FIM and CIS benchmark target.

macos-agent	macOS	001	External laptop; session/auth monitoring.

debian-agent	Debian 12	005	VMware VM on win-agent;  general syslog ,headless os.

lubuntu-agent	Lubuntu	002	VMware VM on win-agent; general syslog / AppArmor.

mint-agent	Linux Mint	004	VMware VM on win-agent; general syslog.

<img width="2828" height="1328" alt="Agents" src="https://github.com/user-attachments/assets/ee106810-e7da-4412-8162-be2123ea5eef" />

Tailnet Layout
<img width="662" height="621" alt="layout drawio" src="https://github.com/user-attachments/assets/cae3d2b0-ac8d-44e4-b2aa-e638e731a413" />
