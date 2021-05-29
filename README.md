# Ansible Role: iiq_db
Deploy a Docker instance of MySQL to be used in an IdentityIQ Sandbox environment

## Requirements

You must have Docker installed to use this role

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    db_volume_name: sandbox_iiq_db_data

Name of the volume for the MySQL data directory.  Usually overriden in the format of <company name>_iiq_db_data

    mssqlbackups_volume_name: sandbox_iiq_db_mssqlbackups

Name of the MS SQL Backups Volume.  This is only used if the db_type is mssql

    db_container_name: sandbox_iiq_db

Name of the MySQL container.  Usually overriden in the format of <company name>_iiq_db

    db_port: 3306

The exposed MySQL port

    db_admin_password: P@ssword123

The MySQL admin password

    db_image: mysql:8.0.17

The MySQL image to use

    mysql_configdir: ./mysqlconfig

The mysql configuration directory

    network_name: sandbox_iiq
    
Name of the docker network to attach the generated containers to.  Usually overriden in the format of <company name>_iiq

    db_type: mysql

Database type to deploy.  Valid values are mysql and sqlserver