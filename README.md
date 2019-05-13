# Overview
Scriptable databases introduce “infrastructure as a code” into devops practices. Scripts for install cloud couchbase cluster.

# Syntax
All sripts have one required paramenter - *$ConfigPath*. This is the path to config, path can be absolute or relative. 

**Examples of installing aks**
Relative path example (you should be in *piptemplates-devops-envmgmt* folder):
`
./cloud/install_couchbase.ps1 ./config/cloud_config.json
`
Absolute path example:
`
~/pip-templates-db-cloud/cloud/install_couchbase.ps1 ~/pip-templates-db-cloud/config/cloud_config.json
`

**Example delete script**
`
./cloud/destroy_couchbase.ps1 ./config/cloud_config.json
`

Also you can install environment using single script:
`
./create_env.ps1 ./config/cloud_config.json
`

Delete whole environment:
`
./delete_env.ps1 ./config/cloud_config.json
`

If you have any problem with not installed tools - use `install_prereq_` script for you type of operation system.

# Project structure
| Folder | Description |
|----|----|
| Cloud | Scripts related to management cloud environment. | 
| Config | Config files for scripts. Store *example* configs for each environment, recomendation is not change this files with actual values, set actual values in duplicate config files without *example* in name. Also stores *resources* files, created automaticaly. | 
| Lib | Scripts with support functions like working with configs, templates etc. | 
| Templates | Folder for storing templates, such as couchbase deploy and params json files. | 

### Cloud couchbase

* Cloud couchbase config parameters

| Variable | Default value | Description |
|----|----|---|
| env_type | cloud | Type of environment |
| az_region | eastus | Azure region where resources will be created |
| az_subscription | piptemplates-DI | Azure subscription name |
| couchbase_az_resource_group | piptemplates-couchbase-east-us-rg | Couchbase azure resource group name |
| couchbase_az_deployment | piptemplates-couchbase-deployment | Couchbase azure deployment name |
| couchbase_username | piptemplatesadmin | Couchbase username used for login to couchbase dashboard and ssh to vm's |
| couchbase_password | piptemplatesadmin2019# | Couchbase password used for login to couchbase dashboard and ssh to vm's |
| couchbase_server_nodes_count | 3 | Count of worker nodes couchbase cluster |
| couchbase_server_disk_size | 32 | Couchbase nodes disk size |
| couchbase_server_version | 6.0.0 | Couchbase server version |
| couchbase_sync_gw_nodes_count | 1 | Couchbase sync gateway count |
| couchbase_sync_gw_version | 2.1.0 | Couchbase sync gateway version |
| couchbase_vm_size | Standard_DS1_v2 | Couchbase azure virtual machines size |
| couchbase_licence | hourly_pricing | Couchbase licence |
| couchbase_location | eastus | Couchbase azure region |