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

Tailnet Layout:

<img width="656" height="454" alt="image" src="https://github.com/user-attachments/assets/e0770da5-1c60-4065-ae60-a5408fb2fa49" />

Snippets of Agent setting up process:

<img width="518" height="187" alt="Screenshot 2026-08-24 143442" src="https://github.com/user-attachments/assets/069df348-3cf6-413a-9d03-138dda49c7a1" />
<img width="524" height="308" alt="Screenshot 2026-08-24 143412" src="https://github.com/user-attachments/assets/42f10c89-84f2-414d-a60c-cd22f3f4817f" />

The Linux mint user will be the focus target of this project. It will receive special attention and more scrutiny than the others.Most of the tests and Client-Server Experiments will be done on it.
