Provides a mechanism to start multiple Docker [[docker]] containers along with storage and networking for the containers to make use of.
# Docker-Compose
...

## Networking
By default Docker-Compose will create a new network for the given compose file. You can change the behaviour by defining custom networks in your compose file.
### Create and assign custom network
...
*Example:*
```yaml
networks:
  custom-network:

services:
  app:
    networks:
      - custom-network
```
### Use existing networks
If you want to use an existing Docker network for your compose files, you can add the `external: true` parameter in your compose file
*Example:*
```yaml
networks:
  existing-network:
    external: true
```

## Volumes
Volumes allow Docker containers to use persistent storage. In a compose file, you can create and map volumes like this:
```yaml
volumes:
  my-volume:

services:
  app:
    volumes:
      - my-volume:/path-in-container
```

These volumes are stored in `/var/lib/docker/volumes`.


#docker 