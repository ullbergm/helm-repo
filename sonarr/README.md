# Sonarr TV Show manager

This is a helm chart for [Sonarr](https://sonarr.tv/).

## Installing

To install the chart:

```bash
helm install --name sonarr ullbergm/sonarr
```

## Uninstalling

To uninstall the chart:

```bash
helm delete --purge sonarr
```

## Configuration

The following tables lists the configurable parameters of the Sentry chart and their default values.

| Parameter                         | Description                         | Default |
|-----------------------------------|-------------------------------------|---------|
| `image.repository`                | Image repository                    | `linuxserver/sonarr` |
| `image.tag`                       | Image tag.                          | `154` |
| `image.pullPolicy`                | Image pull policy                   | `IfNotPresent` |
| `runtime.timezone`                | Timezone                            | `UTC` |
| `runtime.puid`                    | Process User ID                     | `911` |
| `runtime.pgid`                    | Process Group ID                    | `911` |
| `storage.config.storageClassName` | Storage class for the config PVC    | `rook-ceph-block` |
| `storage.config.size`             | Storage size for the config PVC     | `1Gi` |
| `storage.media.server`            | Media NFS host                      | `{}` |
| `storage.media.path`              | Media NFS share                     | `{}` |
| `storage.downloads.server`        | Downloads NFS host                  | `{}` |
| `storage.downloads.path`          | Downloads NFS share                 | `{}` |
| `backup.password`                 | Stash backup password               | `{}` |
| `backup.s3.access_key_id`         | Backup S3 access_key_id             | `{}` |
| `backup.s3.secret_access_key`     | Backup S3 secret_access_key         | `{}` |
| `backup.s3.bucket`                | Backup S3 bucket                    | `{}` |
| `backup.s3.endpoint`              | Backup S3 endpoint                  | `{}` |
| `backup.s3.prefix`                | Backup S3 prefix                    | `{}` |
| `ingress.enabled`                 | Enables Ingress                     | `false` |
| `ingress.path`                    | Ingress path                        | `/` |
| `ingress.hosts`                   | Ingress accepted hostnames          | `chart-example.local` |
