# K3S
Lightweight Kubernetes ([[kubernetes]]). Production ready, easy to install, half the memory, all in a binary less than 100 MB.

Project Homepage: [K3s.io](https://www.k3s.io/)
Documentation: [K3s Documentation](https://docs.k3s.io/)

---
## Installation
To install k3s, you can follow different approaches.

**K3s with external DB ([[k3s-install-ha-externaldb]])** - Set up an HA K3s cluster backed by an external datastore such as MySQL, PostgreSQL, or etcd.

**K3s with embedded DB ([[k3s-install-ha-embeddeddb]])** - Set up an HA K3s cluster that leverages a built-in distributed database.

**K3s single node** ([[k3s-install-single]]) -Set up K3s as a single node installation.

---
## Manage K3S
### Management on Server Nodes
`k3s kubectl`

### Download Kube Config
`/etc/rancher/k3s/k3s.yaml`


## Database Backups

### etcd snapshots
Stored in `/var/lib/rancher/k3s/server/db/snapshots`.


# Certificate Rotation
## Automatic rotation
By default, certificates in K3s expire in 12 months.

If the certificates are expired or have fewer than 90 days remaining before they expire, the certificates are rotated when K3s is restarted.

## Manual rotation
To rotate the certificates manually, use the `k3s certificate rotate` subcommand:
```bash 
# Stop K3s  
systemctl stop k3s  
# Rotate certificates  
k3s certificate rotate  
# Start K3s  
systemctl start k3s
```