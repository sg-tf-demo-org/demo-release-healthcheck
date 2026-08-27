# demo-release-healthcheck

GitOps manifests for the **release healthcheck / Argo CD timeout** Aiden demo.

| Branch | `DATABASE_HOST` | Expected |
|--------|-----------------|----------|
| `main` | `postgres` | Healthy |
| `release` | `postgres-wrong` | `auth-service` CrashLoopBackOff |

Argo CD Application `release-healthcheck` syncs **`release`** → namespace `release-healthcheck` on field-engineering EKS.

See [Infra-Provisioning docs](https://github.com/sg-tf-demo-org/Infra-Provisioning/blob/main/docs/demo-release-healthcheck.md).
