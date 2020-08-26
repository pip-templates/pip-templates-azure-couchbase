# Overview

This is a built-in module to environment [pip-templates-env-master](https://github.com/pip-templates/pip-templates-env-master). 
This module stores scripts for management cloud couchbase cluster.

# Usage

- Download this repository
- Copy *src* and *templates* folder to master template
- Add content of *.ps1.add* files to correspondent files from master template
- Add content of *config/config.db.json.add* to json config file from master template and set the required values

# Config parameters

Config variables description

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
