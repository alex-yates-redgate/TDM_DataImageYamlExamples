# TDM_DataImageYamlExamples
A collection of YAML files for creating data images using the Test Data Manager Cloning Cluster.

Documentation is here:
https://documentation.red-gate.com/redgate-clone/using-the-cli/cli-how-to/creating-a-data-image/data-image-definition-schema-reference

# Examples

## Empty MySQL
To create an empty mysql image, run the command:
    > rgclone create data-image -f ./YAML_Examples/mysql-empty.yml

## Oracle, with HR sample database
To create an oracle image, containing the sample HR database, save an RMAN backup of the Oracle HR sample database to:
    //<your_NFS_or_SMB_file_share>/oracle/hr_backup
Then, run the following command:
    > rgclone create data-image -f ./YAML_Examples/oracle-hr.yml

## SQL Server, with AdventureWorks sample database
To create a Postgres image, containing the sample Pagila database, save a SQL Dunp backup of the Pagila sample database to:
    //<your_NFS_or_SMB_file_share>/postgres/dump-pagila.sql
Then, run the following command:
    > rgclone create data-image -f ./YAML_Examples/postgres-pagila.yml

## Postgres, with Pagila sample database
To create a Postgres image, containing the sample Pagila database, save a SQL Dunp backup of the Pagila sample database to:
    //<your_NFS_or_SMB_file_share>/postgres/dump-pagila.sql
Then, run the following command:
    > rgclone create data-image -f ./YAML_Examples/postgres-pagila.yml