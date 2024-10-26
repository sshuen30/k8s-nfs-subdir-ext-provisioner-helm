# k8s-nfs-subdir-ext-provisioner-helm
This command installs the NFS Subdir External Provisioner chart into the Kubernetes cluster, configuring it to use the specified NFS server
and path for dynamic provisioning of PersistentVolumes
```bash
helm install nfs-subdir-external-provisioner \
nfs-subdir-external-provisioner/nfs-subdir-external-provisioner \
--set nfs.server=172.16.44.32 \
--set nfs.path=/backup/mariadbsc \
--set storageClass.onDelete=true \
--set storageClass.name="nfs-32" -n nfs-provisioner
```
