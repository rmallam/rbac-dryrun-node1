# rbac-dryrun-node1

RBAC dry run

## Pipeline

Jenkinsfile stages: **Install → Lint → Unit tests → SonarQube → Helm lint**.

Point a Jenkins job named `demo/rbac-dryrun-node1` at this repo. Set credential `SONAR_TOKEN` to run the scanner against `http://sonarqube.sonarqube.svc:9000`.

## Deploy

```bash
helm upgrade --install rbac-dryrun-node1 chart -n demo-dev
```

The chart labels pods `backstage.io/kubernetes-id=rbac-dryrun-node1` for Topology.

## Dev Spaces

https://devspaces.apps.rosa.rosa-89s85.bhg0.p3.openshiftapps.com#https://github.com/rmallam/rbac-dryrun-node1?new&devfilePath=devfile.yaml
