# Configuration steps
These are more general OpenShift commands

[Source](https://docs.openshift.com/container-platform/4.2/storage/persistent_storage/persistent-storage-local.html)

## Adding storage
First login as admin with the password you received when starting CRC. 

```
oc login -u kubeadmin -p xxxxx-xxxxx-xxxxx-xxxxx https://api.crc.testing:6443
```

Create a new project:
```
oc new-project local-storage
```

Apply the yaml file
```

```