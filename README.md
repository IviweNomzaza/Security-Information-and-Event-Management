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

Sample Overview of the entire project:
Threat intelligence 
<img width="1524" height="747" alt="Screenshot 2026-09-01 at 23-20-00 Wazuh" src="https://github.com/user-attachments/assets/f7734d6c-7cba-4eb7-b025-afa835f07418" />

<img width="1514" height="747" alt="Screenshot 2026-09-01 at 23-02-59 Wazuh" src="https://github.com/user-attachments/assets/1b732dbd-573c-4cc0-80fe-343f291c74b0" />
<img width="1525" height="815" alt="Screenshot 2026-09-01 at 23-21-38 Wazuh" src="https://github.com/user-attachments/assets/54d04b20-f0ce-4466-80d8-a09e58b06aa1" />

SecOps

<img width="1525" height="1039" alt="Screenshot 2026-09-01 at 23-31-09 Wazuh" src="https://github.com/user-attachments/assets/5d05e7fd-5322-4db5-baf7-154eb7cb217c" />
<img width="1525" height="823" alt="Screenshot 2026-09-01 at 23-46-07 Wazuh" src="https://github.com/user-attachments/assets/61a5edc8-546a-4e25-8099-bb29a7418443" />

<img width="1484" height="749" alt="Screenshot 2026-09-01 at 23-48-45 Wazuh" src="https://github.com/user-attachments/assets/1356a2a2-c523-4c84-a83b-885f36457a79" />

EndPoint Security

<img width="1520" height="932" alt="Screenshot 2026-09-01 at 22-03-21 Wazuh" src="https://github.com/user-attachments/assets/0e6040ae-d6a0-47d4-a44f-15a9e19a6f65" />

<img width="1522" height="846" alt="Screenshot 2026-09-01 at 22-00-04 Wazuh" src="https://github.com/user-attachments/assets/f4b8f69c-7a43-4613-bedf-7ad355889852" />



