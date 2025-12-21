**Week 1 - System Planning and Distribution Selection**

#Virtual Machine
- Ubuntu Server 24.04 LTS (CLI Only)
- Ubuntu Desktop 24.04 LTS (GUI Workstation)

#Network Configuration
- For the server and workstation Host-Only Network
- Verified IP address using 'ip addr'

#SSH Configuration
- Ubuntu desktop (workstation) was connected via SSH
- OpenSSH server on ubuntu server was installed and enabled

#Evidence
<img width="1274" height="801" alt="server ssh running" src="https://github.com/user-attachments/assets/73f38f59-d4f5-49f3-80bc-1e67b0796d3e" />
<img width="1697" height="678" alt="image" src="https://github.com/user-attachments/assets/84c21ed1-b3d4-46e2-b2d8-526c36b4d861" />


**Week 2 - User Management and Privileges**
#Objective
- Learning Linux user and group management
- Configure user privileges using sudo
- Verify access control using CLI

#Tasks
- Creating new users using 'adduser'
- Creating groups using 'groupadd'
- Verified sudo access

#Commands Used
- bash
- add user testuser
- groupadd devgroup
- su - testuser

#Evidence
<img width="755" height="397" alt="add student1" src="https://github.com/user-attachments/assets/3bcf1edf-7fc3-4986-b95e-9126d8cb56a6" />
<img width="1311" height="682" alt="student" src="https://github.com/user-attachments/assets/7955e1f3-3917-4843-8986-8700013a5fb5" />
<img width="531" height="136" alt="student1" src="https://github.com/user-attachments/assets/7cf22023-277c-4762-b6fc-f54d56ee5b92" />

#Reflection
It helped me to understand how linux controls access and privileges using users, groups, and sudo. Managing permissions on the server improved my confident with system administration tasks.

**#Week-3 File Management and Permissions**

#Objective: To Understand linux file systems, ownership, and permission management using command-line tools

#Tasks
- created directories and file using 'mkdir' and 'touch'
- viewed default permission with 'ls -l'
- changed ownership using 'chown'

#Commands used
- mkdir
- touch
- ls -l
- chmod
- chown

#Evidence
<img width="1083" height="672" alt="A" src="https://github.com/user-attachments/assets/4a6397aa-161d-4471-a553-027c5fd796a1" />
<img width="900" height="438" alt="b" src="https://github.com/user-attachments/assets/25b6aa07-4eff-414a-90df-bcfc1623c604" />

**#Week 4 - File Compression and Archiving**

#objective
The aim of Week 4 was to implement foundational security controls on a headless Linux server and demonstrate secure remote administration using SSH. All administrative tasks were performed remotely from a dedicated Ubuntu Desktop workstation via the command-line interface, in line with the coursework requirements.
The server system runs without a graphical interface, enforcing command-line proficiency and reflecting real-world professional server administration practices.

#user and privilage management
To minimise security risks associated with direct root access, a non-root administrative user was created and granted sudo privileges. This follows the principle of least privilege and reduces the likelihood of accidental system-wide changes.

#Comands
bash
sudo adduser adminuser
sudo usermod -aG sudo adminuser
group adminuser

#Evidence
<img width="1561" height="861" alt="w4" src="https://github.com/user-attachments/assets/2106c8de-4316-4c44-bb9f-9a819bd83502" />
<img width="1423" height="816" alt="wk 4" src="https://github.com/user-attachments/assets/a8994e1c-d7ba-427e-af38-2eae4f480b0b" />
<img width="1665" height="851" alt="wke4" src="https://github.com/user-attachments/assets/57832ba3-ea6a-4948-a3a7-2a735b454a6e" />

**#Week-5 Process Management**

#Objective
The aim of Week 5 was to extend the foundational security implemented in Week 4 by deploying advanced security mechanisms and introducing automation for security verification and system monitoring. All configuration and administration tasks were performed remotely on a headless Ubuntu Server via SSH from an Ubuntu Desktop workstation, ensuring compliance with the coursework administrative constraints.

#Mandatory Access Control – AppArmor
Mandatory Access Control (MAC) was implemented using AppArmor. AppArmor restricts the actions applications can perform, even if they are compromised, providing an additional layer of defence beyond traditional file permissions.

#Evidence
<img width="1626" height="863" alt="w5" src="https://github.com/user-attachments/assets/cc60090a-66de-40f3-bd5d-aa34eb94f1bc" />
<img width="1821" height="832" alt="we5" src="https://github.com/user-attachments/assets/efe539c6-eadd-4c25-8c6f-faa8da119420" />
<img width="1572" height="856" alt="week5" src="https://github.com/user-attachments/assets/d1130be1-c217-4078-abf2-4b1042d708a0" />
<img width="1452" height="947" alt="wee5" src="https://github.com/user-attachments/assets/73a11b35-634a-4d75-85ef-aea96f9d2738" />
<img width="1722" height="872" alt="wk5" src="https://github.com/user-attachments/assets/3ba035d4-eef5-4feb-b7c5-8a69bc956ce9" />

#Installation
sudo apt install -y fail2ban
sudo systemctl enable fail2ban
sudo systemctl start fail2ban

#Status Verification
sudo systemctl status fail2ban
sudo fail2ban-client status
sudo fail2ban-client status sshd



