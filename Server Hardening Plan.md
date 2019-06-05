# Server Hardening Plan

### Index
- Overview
##### Steps to Take
- [Create a New User](#create-new-user)
- [Disable Root Logon](#disable-root-logon)
- [Setup Key Based Logon](#setup-key-based-logon)
- Disable Password Based Logon
- Change SSH Port
- Limit SSH to certain Users
- Set SSH Idle Timeout
- Disable Empty Passwords
- Disable Rhosts
- Disable Host Based Authentication
- Enable and Configure UFW
- Enable and Configure GeoIP
- Enable and Configure Fail2Ban
<br><br>
##### Create New User
Create another user and add them to the Sudo Group<br>
`sudo adduser "Username"` <br>
`sudo usermod -aG sudo "Username"`

##### Disable Root Logon
Open /etc/ssh/sshd_config and change "PermitRootLogon" to no
(picture)

##### Setup Key Based Logon
Create a new key pair on your local machine
`sudo ssh-keygen`<br>
![ssh keygen image](/images/ssh_keygen.png)<br>
Copy the key to the server<br>
`ssh-copy-id user@hostname`
