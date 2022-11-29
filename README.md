# diego-tooling-template

Core template fields:

 * `{{{ ORG_NAME }}}` the name of the customer Github Organisation
 * `{{{ DOMAIN }}}` the customer domain
 * `{{{ CLUSTER_NAME }}}` the cluster name where diego will be insttalled
 * `{{{ R53_ZONE_ID }}}` the diego R53 zone
 * `{{{ AWS_ACCOUNT_ID }}}` the customers AWS account ID where Diego will be installed


## secrets

Secrets for Diego API, Diego Application Controller and Dex must be present in the cluster. These secrets are not created as part of this repo.

The secrets referenced are:

- `diego-api`, a mix of config and sensitive ArgoCD user name and password. Used by Diego API
- `github-app`, a mix of cofig and sensitive private key. Used by both the Diego API and the application controller
- `dex-github-oauth`, sensitive client id and secret of the Diego Github App. Used by Dex. 
- `dex-static-clients-oauth`, sensitive client id and secret of ArgoCD as a registered cleint of Dex. Used by Dex.
