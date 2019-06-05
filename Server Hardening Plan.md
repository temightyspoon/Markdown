# Server Hardening Plan

### Index
- Overview
##### Steps to Take
- [Create a New User](#create-new-user)
- [Disable Root Logon](#disable-root-logon)
- Enable Key Based Logon
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
`sudo adduser "Username"`<br>
`sudo usermod -aG sudo "Username"`

##### Disable Root Logon
Open /etc/ssh/sshd_config and change "PermitRootLogon" to no
(picture)
