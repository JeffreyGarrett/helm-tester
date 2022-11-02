# calarm-collection-cis

![Version: 1.0.5](https://img.shields.io/badge/Version-1.0.5-informational?style=flat-square) ![AppVersion: 2.0](https://img.shields.io/badge/AppVersion-2.0-informational?style=flat-square)

Calarm Collection CIS Module

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| JeffreyGarrett | <jeff.garrett@dhcs.ca.gov> |  |

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| @bitnami | calarm-db(postgresql) | 10.14.3 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| calarm-db."service.port" | int | `5432` |  |
| calarm-db.postgresqlDatabase | string | `"cisdev"` |  |
| calarm-db.postgresqlPassword | string | `"COLLPLUSCGIDBCISDEV"` |  |
| calarm-db.postgresqlUsername | string | `"cisown"` |  |
| cisSecret | string | `"secret-dev-calarmcollectioncis"` |  |
| dbmigrations.command[0] | string | `"sh"` |  |
| dbmigrations.command[1] | string | `"-c"` |  |
| dbmigrations.command[2] | string | `"echo \"Start - Run CIS postgres db migrations!\"\nsleep 30\n# exit 1\necho \"End - Run CIS postgres db migrations!\"\n"` |  |
| dbmigrations.enabled | bool | `true` |  |
| dbmigrations.image | string | `"166636506311.dkr.ecr.us-west-2.amazonaws.com/busybox:0.0.1-scuttle"` |  |
| gateway.domainWildcard | string | `"calarm-cis.cammis-mod-dev.dhcs.ca.gov"` |  |
| global.awsRegion | string | `"us-west-2"` |  |
| global.postgresql | object | `{}` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.repository | string | `"166636506311.dkr.ecr.us-west-2.amazonaws.com/calarm-collection-cis:c603e59"` |  |
| postgresql.auth.database | string | `"cisdev"` |  |
| postgresql.persistence.enabled | bool | `false` |  |
| replicaCount | int | `1` |  |
| resources.limits.cpu | int | `4` |  |
| resources.limits.memory | string | `"4Gi"` |  |
| resources.requests.cpu | int | `2` |  |
| resources.requests.memory | string | `"2Gi"` |  |
| service.hosts | string | `"calarm-cis.cammis-mod-dev.dhcs.ca.gov"` |  |
| service.port | int | `8080` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)