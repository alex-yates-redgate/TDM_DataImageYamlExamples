# TDM_DataImageYamlExamples
A collection of YAML files for creating data images using the Test Data Manager Cloning Cluster.

Documentation is here:
https://documentation.red-gate.com/redgate-clone/using-the-cli/cli-how-to/creating-a-data-image/data-image-definition-schema-reference

# Examples

## Empty containers
To create an empty image, run one of the following commands:

```
    > rgclone create data-image -f ./YAML_Examples/mssql-empty.yml
    > rgclone create data-image -f ./YAML_Examples/mysql-empty.yml
    > rgclone create data-image -f ./YAML_Examples/oracle-empty.yml
    > rgclone create data-image -f ./YAML_Examples/postgres-empty.yml
```

Note: Some of these have default lifetimes set in the YAML. Check the files for details!

## Containers with sample databases
To create an image from a backup, first, check the YAML file for your RDBMS:
- MS SQL:   ./YAML_Examples/mssql-adventureworks.yml
- MySQL:    ./YAML_Examples/mysql-sakila.yml
- Oracle:   ./YAML_Examples/oracle-hr.yml
- Postgres: ./YAML_Examples/postgres-pagila.yml

Note the backup paths. For example, for MS SQL:

```
    backups:
    - path: mssql/AdventureWorks.bak
``` 

Ensure a native backup is saved to the appropriate location on the fileshare that was set up for your cloning cluster. For example, for MS SQL / AdventureWorks:

```
   //<your_NFS_or_SMB_file_share>/mssql/AdventureWorks.bak
```

Then, run the rgclone create data-image command, referencing the apropriate YAML file. For example, for MS SQL:
 
```
    > rgclone create data-image -f ./YAML_Examples/mssql-adventureworks.yml
```