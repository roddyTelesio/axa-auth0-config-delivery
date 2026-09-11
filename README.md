# Auth0 Configuration Delivery (DEV → STAGING)

This repository automatically deploys Auth0 configurations from the DEV tenant to STAGING
using the Auth0 Deploy CLI running within GitHub Actions.

## How to deploy?

1. Go to the **Actions** tab
2. Select **Auth0 Config Delivery (DEV → STAGING)**
3. Click **Run workflow**
4. Choose "confirm_import: yes"
5. Click **Run workflow**
6. Wait for the `Export configs from DEV` job ✅
7. Approve the `staging` environment (Review deployments)
8. Wait for the `Import configs to STAGING` job ✅
9. Verify in the Auth0 STAGING Dashboard

## Security

- ❌ Never commit secrets to `config/`
- ✅ Secrets stored in **Settings > Secrets and variables > Actions**
- ✅ `AUTH0_ALLOW_DELETE: false` to prevent any deletions
- ✅ `staging` environment with required reviewers

## Contact

RRA TELESIO
