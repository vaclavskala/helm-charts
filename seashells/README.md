
# Seashells server

Helm chart for deploying seashells server (https://seashells.io/)

Original project github: https://github.com/anishathalye/seashells-server

This chart is made with improvements from this PR: https://github.com/anishathalye/seashells-server/pull/4

## Quickstart
To install the seashells chart with default options:
```
helm repo add seashells https://vaclavskala.github.io/helm-charts/
helm repo update
helm install my-seashells seashells/seashells
```

## Configuration
To install the seashells chart with customized options:
1, Download default values:
```
helm show values seashells/seashells > values.yaml
```
2, Customize values

3, Install with customized values
```
helm install my-seashells seashells/seashells --values values.yaml
```

## Paremeters
|              Parameter       |                    Description                     |                     Default                      |
| ---------------------------- | -------------------------------------------------- | ------------------------------------------------ |
| `config.baseUrl`             | On which URL server content                        | `http://seashells.local/v/`                      |
| `config.ncPort`              | On which port listen for netcat input              | `1337`                                           |
| `config.ginMode`             | https://gin-gonic.com/                             | `release`                                        |
| `auth.adminPassword`         | Password for /inspect                              | `empty (/inspect disabled)`                      |
| `auth.existingSecret`        | Read admin password from existing secret           | `empty (/inspect disabled)`                      |
