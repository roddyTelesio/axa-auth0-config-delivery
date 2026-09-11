# Auth0 Config Delivery (DEV → STAGING)

Ce repo livre automatiquement les configurations Auth0 du tenant DEV vers STAGING
via le Auth0 Deploy CLI exécuté dans GitHub Actions.

## Comment livrer ?

1. Va dans l'onglet **Actions**
2. Sélectionne **Auth0 Config Delivery (DEV → STAGING)**
3. Clique sur **Run workflow**
4. Choisis `confirm_import: yes`
5. Clique sur **Run workflow**
6. Attends le job `Export configs from DEV` ✅
7. Approuve l'environment `staging` (Review deployments)
8. Attends le job `Import configs to STAGING` ✅
9. Vérifie dans le Dashboard Auth0 STAGING

## Sécurité

- ❌ Ne jamais commiter de secrets dans `config/`
- ✅ Secrets dans **Settings > Secrets and variables > Actions**
- ✅ `AUTH0_ALLOW_DELETE: false` pour éviter toute suppression
- ✅ Environment `staging` avec Required reviewers

## Contact

RRA TELESIO 
