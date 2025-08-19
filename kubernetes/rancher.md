Provides the ability to manage multiple Kubernetes [[kubernetes]] clusters.
# Install Rancher in single mode

Execute the following script to backup the defined version and install the upgrade version.

```bash
#!/bin/bash
RANCHER_VERSION="v2.5.9"
RANCHER_UPGRADE_VERSION="v2.6.9"
RANCHER_CONTAINER_NAME=$(sudo docker ps --format {{.Names}})
TIMESTAMP=$(date --iso-8601=seconds)

echo "RANCHER_VERSION: $RANCHER_VERSION"
echo "RANCHER_CONTAINER_NAME: $RANCHER_CONTAINER_NAME"
echo "RANCHER_CONTAINER_TAG: $RANCHER_CONTAINER_TAG"

echo "Backing up"
echo "Rollback procedure documented at https://docs.ranchermanager.rancher.io/how-to-guides/new-user-guides/backup-restore-and-disaster-recovery/restore-docker-installed-rancher"

sudo docker stop $RANCHER_CONTAINER_NAME
sudo docker create --volumes-from $RANCHER_CONTAINER_NAME --name rancher-data rancher/rancher:$RANCHER_VERSION
sudo docker run --volumes-from rancher-data -v $PWD:/backup busybox tar pzcvf /backup/rancher-data-backup-$RANCHER_VERSION-$TIMESTAMP.tar.gz /var/lib/rancher

echo "Upgrading..."
sudo docker pull rancher/rancher:$RANCHER_UPGRADE_VERSION
sudo docker run -d --privileged --volumes-from rancher-data --restart=unless-stopped  -p 80:80 -p 443:443  rancher/rancher:$RANCHER_UPGRADE_VERSION

echo "Done"
```



