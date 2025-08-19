# Helm

Provides a way to find, share, and use software built for Kubernetes [[kubernetes]].
# Helm Cheat-Sheet
## Repository Management

| Command | Description |
| --- | --- |
| `helm repo list` | List Helm repositories |
| `helm repo update` | Update list of Helm charts from repositories |

## Chart Management

| Command | Description |
| --- | --- |
| `helm search` | List all installed charts |
| `helm search <chart>` | Search for a chart |
| `helm ls` | List all installed Helm charts |
| `helm ls --deleted` | List all deleted Helm charts |
| `helm ls --all` | List installed and deleted Helm charts |
| `helm inspect values <repo>/<chart>` | Inspect the variables in a chart |

## Install/Delete Helm Charts

| Command | Description |
| --- | --- |
| `helm install --name <name> <repo>/<chart>` | Install a Helm chart |
| `helm install --name <name> --values <VALUES.YML> <repo>/<chart>` | Install a Helm chart and override variables |
| `helm status <name>` | Show status of Helm chart being installed |
| `helm delete --purge <name>` | Delete a Helm chart |

## Upgrading Helm Charts

| Command | Description |
| --- | --- |
| `helm get values <name>` | Return the variables for a release |
| `helm upgrade --values <file> <name> <repo>/<chart>` | Upgrade the chart or variables in a release |
| `helm history <name>` | List release numbers |
| `helm rollback <name> 1` | Rollback to a previous release number |

## Creating Helm Charts

| Command | Description |
| --- | --- |
| `helm create <name>` | Create a blank chart |
| `helm lint <name>` | Lint the chart |
| `helm package <name>` | Package the chart into foo.tgz |
| `helm dependency update` | Install chart dependencies |

COMMAND | DESCRIPTION
---|---
`helm create <NAME>` | Create a blank chart
`helm lint <NAME>` | Lint the chart
`helm package <NAME>` | Package the chart into foo.tgz
`helm dependency update` | Install chart dependencies

## Chart Folder Structure
```
wordpress/
  Chart.yaml          # A YAML file containing information about the chart
  LICENSE             # OPTIONAL: A plain text file containing the license for the chart
  README.md           # OPTIONAL: A human-readable README file
  requirements.yaml   # OPTIONAL: A YAML file listing dependencies for the chart
  values.yaml         # The default configuration values for this chart
  charts/             # A directory containing any charts upon which this chart depends.
  templates/          # A directory of templates that, when combined with values,
                      # will generate valid Kubernetes manifest files.
  templates/NOTES.txt # OPTIONAL: A plain text file containing short usage notes
```

#kubernetes 