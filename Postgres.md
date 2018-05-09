# Postgres

## Index
* [Installation in RedHat](#installation-in-redhat)

## Installation in RedHat
1. Install the repository RPM:

``sudo yum install https://download.postgresql.org/pub/repos/yum/9.6/redhat/rhel-7-x86_64/pgdg-redhat96-9.6-3.noarch.rpm``

2. Install the client packages:

``sudo yum install postgresql96``

3. install the server packages: 

``sudo yum install postgresql96-server``

4. Initialize the database and enable automatic start:

``sudo /usr/pgsql-9.6/bin/postgresql96-setup initdb``

``sudo systemctl enable postgresql-9.6``  
``sudo systemctl start postgresql-9.6``

5. Get log into postgres with the postgres user 

``sudo -u postgres psql``

6. Change the postgres user’s password 
```console
psql (9.6.6)
Type "help" for help.
 
postgres=# ALTER USER postgres WITH PASSWORD 'xxxxxxxxx';
```

7. Configure the postgres to access from outside the localhost:

Modify the ``postgresql.conf`` file  
Set the ``listen_addresses`` parameter to ``*``  
The file is located in ``/var/lib/pgsql/9.6/data``

8. Modify the pg_hba.conf file
```console
# "local" is for Unix domain socket connections only
local   all             all                                     trust
# IPv4 local connections:
host    all             all             127.0.0.1/32            trust
host    all             all             0.0.0.0/0               md5
```
The file is located in ``/var/lib/pgsql/9.6/data``

9. Restart the postgres service to apply the changes:

``sudo systemctl restart postgresql-9.6``

10. Configure the firewall:

``sudo firewall-cmd --zone=public --add-port=5432/tcp --permanent`` 
``sudo firewall-cmd --reload`` 
