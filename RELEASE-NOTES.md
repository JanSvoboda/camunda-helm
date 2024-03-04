The changelog is automatically generated using [git-chglog](https://github.com/git-chglog/git-chglog)
and it follows [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) format.


<a name="camunda-platform-9.2.0"></a>
## [camunda-platform-9.2.0](https://github.com/camunda/camunda-platform-helm/compare/camunda-platform-9.1.2...camunda-platform-9.2.0) (2024-02-29)

### Feat

* support custom pvc annotations for Zeebe ([#1359](https://github.com/camunda/camunda-platform-helm/issues/1359))
* console sm alpha ([#1334](https://github.com/camunda/camunda-platform-helm/issues/1334))

### Fix

* moves ccsm spring profile outside of conditional ([#1337](https://github.com/camunda/camunda-platform-helm/issues/1337))
* update to use initialContactPoints for Zeebe Gateway ([#1353](https://github.com/camunda/camunda-platform-helm/issues/1353))
* update version matrix after latest bugfix releases ([#1358](https://github.com/camunda/camunda-platform-helm/issues/1358))
* separated ingress status in helm notes ([#1318](https://github.com/camunda/camunda-platform-helm/issues/1318))

### Test

* remove old console test config
* disable prometheus tests until prometheus Completed issue is resolved ([#1350](https://github.com/camunda/camunda-platform-helm/issues/1350))
* fix yamllint errors ([#1345](https://github.com/camunda/camunda-platform-helm/issues/1345))
### Images

Camunda images:

- docker.io/camunda/connectors-bundle:8.4.4
- docker.io/camunda/identity:8.4.4
- docker.io/camunda/operate:8.4.4
- docker.io/camunda/optimize:8.4.1
- docker.io/camunda/tasklist:8.4.4
- docker.io/camunda/zeebe:8.4.4
- registry.camunda.cloud/web-modeler-ee/modeler-restapi:8.4.2
- registry.camunda.cloud/web-modeler-ee/modeler-webapp:8.4.2
- registry.camunda.cloud/web-modeler-ee/modeler-websockets:8.4.2

Non-Camunda images:

- docker.io/bitnami/elasticsearch:8.9.2
- docker.io/bitnami/keycloak:22.0.5
- docker.io/bitnami/os-shell:12-debian-12-r16
- docker.io/bitnami/postgresql:15.6.0

### Verification

To verify integrity of the Helm chart using [Cosign](https://docs.sigstore.dev/signing/quickstart/):

```shell
cosign verify-blob camunda-platform-9.2.0.tgz \
  --bundle camunda-platform-9.2.0.cosign.bundle \
  --certificate-oidc-issuer "https://token.actions.githubusercontent.com" \
  --certificate-identity "https://github.com/camunda/camunda-platform-helm/.github/workflows/chart-release.yaml@refs/pull/1385/merge"
```
