# LabKey
This repo contains some scripts and other information that can be useful when using
Ansible to install LabKey.

## Roles
* common - This role installs Python 2.x, pip and updates the servers
* labkey - This role downloads and installs the LabKey system
* mssql - This role installs mssql on Ubuntu and creates a DB for use with Labkey
* tomcat - This role installs Oracle Java and Tomcat.

##Vault File
A vault file is used for sensitive data:
* '<lbky_aws_url>' - LabKey URL download for your organization.
* '<lbky_home>' - LabKey home on the server.
* '<tomcat_home>' - Tomcat home on the server.
* '<tomcat_mgr_uname>' - Tomcat manager username.
* '<tomcat_mgr_pword>' - Tomcat manager password.
