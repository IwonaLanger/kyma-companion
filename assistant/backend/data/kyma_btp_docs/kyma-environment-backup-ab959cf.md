

# Kyma Environment Backup

The user load on a Kyma cluster typically consists of various Kubernetes objects and volumes. The object backup process is automated, but you need to take care of volume backups so you can recover your customer data.





## Object Backup for Kubernetes Configuration

Kyma environment relies on the managed Kubernetes cluster for periodic backups of Kubernetes objects. Automatic backup doesn't include Kubernetes volumes.

For example, project "Gardener" uses etcd as the Kubernetes' backing store for all cluster data. This means that all Kubernetes objects are stored on etcd. Gardener uses periodic jobs to take major and minor snapshots of the etcd database. A major snapshot \(including all the resources\) takes place every day, and each minor snapshot \(including only the changes in between\) takes place every 5 minutes. If the etcd database experiences any problems, Gardener automatically restores the Kubernetes cluster using the latest snapshot.





## Volume Backup for Customer Data

Your customer data isn't backed up automatically. If you're using Kubernetes volumes to store data, we recommend that you use Kubernetes VolumeSnapshots to backup and recover your data. The backup and recovery using Kubernetes VolumeSnapshots are supported for AWS, Azure, and Google Cloud.

**Related Information**  


[Kyma: Create on-demand volume snapshots](https://kyma-project.io/#/04-operation-guides/operations/10-backup-kyma?id=create-on-demand-volume-snapshots)

[Change Storage Size in Kyma](change-storage-size-in-kyma-027f5e2.md "If the amount of data for the applications in your Kyma environment grows, you can expand the storage size for your customer data by resizing the respective Persistent Volume Claim (PVC).")

