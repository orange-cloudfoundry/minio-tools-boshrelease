# Minio-tools-boshrelease

This is a boshrelease to be use in conjunction with release [minio](https://github.com/minio/minio-boshrelease).

Job included:
- [create-buckets](/jobs/create-buckets/spec): Create buckets on your minio at [post-deploy](https://bosh.io/docs/post-deploy/)
- [mc](/jobs/mc/spec): Job mc let you inspect minio when ssh as root (e.g.: `mc ls myminio`)
- [minio_alerts](/jobs/minio_alerts/spec): Set of alerts for [prometheus-boshrelease](https://github.com/bosh-prometheus/prometheus-boshrelease)
- [minio_dashboards](/jobs/minio_dashboards/spec): Set of grafana dashboards for [prometheus-boshrelease](https://github.com/bosh-prometheus/prometheus-boshrelease)

## Operations files

- [/operations/cf/use-minio-blobstore.yml](/operations/cf/use-minio-blobstore.yml): Include this ops file to your [cf-deployment](https://github.com/cloudfoundry/cf-deployment) to use minio as a cloud foundry blobstore (should be use after ops file https://github.com/cloudfoundry/cf-deployment/blob/master/operations/use-external-blobstore.yml)
- [/operations/prometheus/monitor-minio.yml](/operations/prometheus/monitor-minio.yml): Include this ops file to your [prometheus-deployment](https://github.com/bosh-prometheus/prometheus-boshrelease) to monitor minio in your prometheus

