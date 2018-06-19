# LabKey
This repo contains some scripts and other information to install LabKey on an Ubuntu front end WebServer and an Ubuntu backend with MSSQL.

## Roles
* common - This role installs Python 2.x, pip and updates the servers
* labkey - This role downloads and installs the LabKey system
* mssql - This role installs mssql on Ubuntu and creates a DB for use with Labkey
* tomcat - This role installs Oracle Java and Tomcat.

## Vault File
A vault file is used for sensitive data:
* `<lbky_aws_url>` - LabKey URL download for your organization.
* `<lbky_home>` - LabKey home on the server.
* `<tomcat_home>` - Tomcat home on the server.
* `<tomcat_mgr_uname>` - Tomcat manager username.
* `<tomcat_mgr_pword>` - Tomcat manager password.
* `<jdbcUser>` - JDBC connection user.
* `<jdbcPass>` - JDBC connection password.
* `<pid>` - Type of MS SQL Installation.
* `<tsql_endpoint_port>` - Port for Database.
* `<sa_password>` - SA password.
* `<db_server>` - LabKey MS SQL host.
* `<db_name>` - LabKey database name.

The vault file in the playbooks is located at `</home/cnprc/lbky.yml>` and included in the webserver.yml and mssql.yml playbooks.

## LabKey Tomcat XML
The LabKey tomcat XML in the playbooks is prepopulated and resides at `</home/cnprc/labkey.xml>`

# LabKey Download file.
Ensure to change the name of the file in the `/defaults/main.yml` to reflect the name on your LabKey download page.
Ensure the LabKey URL in the vault file points to your organizations download trunk.

## MS SQL
MS SQL installation requires pip and pymssql be installed on the remote host with the Database.