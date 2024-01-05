# TDM_DataImageYamlExamples
A collection of YAML files for creating data images using the Test Data Manager Cloning Cluster.

Documentation is here:
https://documentation.red-gate.com/redgate-clone/using-the-cli/cli-how-to/creating-a-data-image/data-image-definition-schema-reference

To create an empty mysql image, run the command:
> rgclone create data-image -f ./empty-mysql.yml

To create an empty oracle image, save an RMAN backup of the Oracle HR sample database to:

//<your_NFS_or_SMB_file_share>/oracle/hr_backup

> rgclone create data-image -f ./empty-mysql.yml