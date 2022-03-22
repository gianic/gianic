title: About OAuth App access restrictions
intro: 'Organizations can choose which {% data variables.product.prodname_oauth_apps %} have access to their repositories and other resources by enabling {% data variables.product.prodname_oauth_app %} access restrictions.'
redirect_from:
  - /articles/about-third-party-application-restrictions
  - /articles/about-oauth-app-access-restrictions
  - /github/setting-up-and-managing-organizations-and-teams/about-oauth-app-access-restrictions
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: OAuth App access
---
## About OAuth App access restrictions

When {% data variables.product.prodname_oauth_app %} access restrictions are enabled, organization members cannot authorize {% data variables.product.prodname_oauth_app %} access to organization resources. Organization members can request owner approval for {% data variables.product.prodname_oauth_apps %} they'd like to use, and organization owners receive a notification of pending requests.

{% data reusables.organizations.oauth_app_restrictions_default %}

{% tip %}

Tip: When an organization has not set up {% data variables.product.prodname_oauth_app %} access restrictions, any {% data variables.product.prodname_oauth_app %} authorized by an organization member can also access the organization's private resources.

{% endtip %}

{% ifversion fpt %}
To further protect your organization's resources, you can upgrade to {% data variables.product.prodname_ghe_cloud %}, which includes security features like SAML single sign-on. {% data reusables.enterprise.link-to-ghec-trial %}
{% endif %}

## Setting up {% data variables.product.prodname_oauth_app %} access restrictions

When an organization owner sets up {% data variable
- Applications that are owned by the organization are automatically given access to the organization's resources.
- {% data variables.product.prodname_oauth_apps %} immediately lose access to the organization's resources.
- SSH keys created before February 2014 immediately lose access to the organization's resources (this includes user and deploy keys).
- SSH keys created by {% data variables.product.prodname_oauth_apps %} during or after February 2014 immediately lose access to the organization's resources.
- Hook deliveries from private organization repositories will no longer be sent to unapproved {% data variables.product.prodname_oauth_apps %}.
- API access to private organization resources is not available for unapproved {% data variables.product.prodname_oauth_apps %}. In addition, there are no privileged create, update, or delete actions on public organization resources.
- Hooks created by users and hooks created before May 2014 will not be affected.
- Private forks of organization-owned repositories are subject to the organization's access restrictions.
"[Enabling {% data variables.product.prodname_oauth_app %} access restrictions for your organization](/articles/enabling-oauth-app-access-restrictions-for-your-organization)"
- "[Approving {% data variables.product.prodname_oauth_apps %} for your organization](/articles/approving-oauth-apps-for-your-organization)"
- "[Reviewing your organization's installed integrations](/articles/reviewing-your-organization-s-installed-integrations)"
- "[Denying access to a previously approved {% data variables.product.prodname_oauth_app %} for your organization](/articles/denying-access-to-a-previously-approved-oauth-app-for-your-organization)"
- "[Disabling {% data variables.product.prodname_oauth_app %} access restrictions for your organization](/articles/disabling-oauth-app-access-restrictions-for-your-organization)"
- "[Requesting organization approval for {% data variables.product.prodname_oauth_apps %}](/articles/requesting-organization-approval-for-oauth-apps)"
- "[Authorizing {% data variables.product.prodname_oauth_apps %}](/github/authenticating-to-github/keeping-your-account-and-data-secure/authorizing-oauth-apps)"
- 
- 
