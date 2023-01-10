# diego-tooling-template

Core template fields:

 * `{{{ ORG_NAME }}}` the name of the customer GitHub organisation
 * `{{{ DOMAIN }}}` the customer domain
 * `{{{ CLUSTER_NAME }}}` the cluster name where Diego will be installed
 * `{{{ R53_ZONE_ID }}}` the Diego R53 zone
 * `{{{ AWS_ACCOUNT_ID }}}` the customers AWS account ID where Diego will be installed


## Secrets

Secrets for Diego API, Diego Application Controller and Dex must be present in the cluster. These secrets are not created as part of this repo.

The secrets referenced are:

- `diego-api`, a mix of configuration and sensitive ArgoCD user name and password. Used by Diego API
- `github-app`, a mix of configuration and sensitive private key. Used by both the Diego API and the application controller
- `dex-github-oauth`, sensitive client id and secret of the Diego GitHub App. Used by Dex. 
- `dex-static-clients-oauth`, sensitive client id and secret of ArgoCD as a registered client of Dex. Used by Dex.
