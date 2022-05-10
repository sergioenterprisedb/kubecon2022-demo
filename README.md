# Description
In this demo I'll show you how to create a Postgres cluster with CloudNativePG kubernetes operator. The features that I want to show you are:
- Kubernetes plugin install
- CloudNativePG operator install
- Postgres cluster install
- Insert data in the cluster
- Switchover (promote)
- Failover
- Backup
- Recovery

# Prerequisites
- K8s
- Docker
- In my laptop, I've installed K3d (k3d is a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker).

# Demo
Execute commands in the correct order:
```
. ./01_install_plugin.sh
. ./02_install_operator.sh
. ./03_check_operator_installed.sh
. ./04_get_cluster_config_file.sh
. ./05_install_cluster.sh
```
Open a new session and execute:
```
. ./06_show_status.sh
```
Go back to the previous session and execute:
```
. ./07_insert_data.sh
. ./08_promote.sh
. ./09_upgrade.sh
. ./10_backup_cluster.sh
. ./11_backup_describe.sh
. ./12_restore_cluster.sh
```

To delete your cluster execute:
```
# Warning: script adapted for K3d
. ./99_remove_cluster.sh
```
