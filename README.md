# diego-tooling-template

Core template fields:

 * `{{{ ORG_NAME }}}` the name of the customer Github Organisation
 * `{{{ DOMAIN }}}` the customer domain
 * `{{{ CLUSTER_NAME }}}` the cluster name where diego will be insttalled
 * `{{{ R53_ZONE_ID }}}` the diego R53 zone
 * `{{{ AWS_ACCOUNT_ID }}}` the customers AWS account ID where Diego will be installed


## secrets

The API and Diego application controller secrets must be present in the cluster. These secrets are not created as part of this repo
