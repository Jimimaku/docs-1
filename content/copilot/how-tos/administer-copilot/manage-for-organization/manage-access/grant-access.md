---
title: Granting access to Copilot for members of your organization
shortTitle: Grant access
intro: 'Grant access to {% data variables.product.prodname_copilot %} for some or all of the members of your organization.'
permissions: 'Organization owners for organizations with a {% ifversion ghec %}{% data variables.copilot.copilot_enterprise_short %} or{% endif %} {% data variables.copilot.copilot_business_short %} plan.'
versions:
  feature: copilot
redirect_from:
  - /copilot/managing-github-copilot-in-your-organization/managing-access-for-copilot-in-your-organization
  - /copilot/managing-github-copilot-in-your-organization/managing-access-for-copilot-business-in-your-organization
  - /copilot/managing-copilot-for-business/managing-access-for-copilot-for-business-in-your-organization
  - /copilot/managing-copilot-business/managing-access-for-copilot-business-in-your-organization
  - /copilot/managing-github-copilot-in-your-organization/granting-access-to-copilot-for-members-of-your-organization
  - /copilot/managing-copilot/managing-github-copilot-in-your-organization/granting-access-to-copilot-for-members-of-your-organization
  - /copilot/managing-copilot/managing-github-copilot-in-your-organization/managing-access-to-github-copilot-in-your-organization/granting-access-to-copilot-for-members-of-your-organization
  - /copilot/how-tos/administer/organizations/managing-access-to-github-copilot-in-your-organization/granting-access-to-copilot-for-members-of-your-organization
  - /copilot/how-tos/administer/organizations/managing-access-to-github-copilot-in-your-organization/grant-access
  - /copilot/how-tos/administer/organizations/manage-access/grant-access
  - /copilot/how-tos/administer/manage-for-organization/manage-access/grant-access
topics:
  - Copilot
contentType: how-tos
---

## Configuring access to {% data variables.product.prodname_copilot %} in your organization

{% ifversion ghec %}After a {% data variables.product.prodname_dotcom %} enterprise owner enables {% data variables.copilot.copilot_enterprise_short %} or {% data variables.copilot.copilot_business_short %} for an organization, an owner of that organization can grant {% data variables.product.prodname_copilot %} access to members of their organization.{% else %}After setting up a {% data variables.copilot.copilot_business_short %} plan, an organization owner can grant {% data variables.product.prodname_copilot %} access to members of their organization.{% endif %}

Billing for {% data variables.product.prodname_copilot %} starts when you grant an organization member access, irrespective of when they first use {% data variables.product.prodname_copilot_short %}. If you grant an organization member access midway through a billing cycle, the cost is prorated for the remainder of the cycle. For more information, see [AUTOTITLE](/billing/managing-billing-for-github-copilot/about-billing-for-github-copilot).

## Granting access to {% data variables.product.prodname_copilot %} for all current and future users in your organization

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.copilot.access-settings %}
1. If the **Allow this organization to assign seats** button is displayed, click this button.
1. Click **Start adding seats**.
1. To enable {% data variables.product.prodname_copilot %} for all current and future users in your organization, select **Purchase for all members**.
1. In the "Confirm seats purchase for all members" dialog, to confirm that you want to enable {% data variables.product.prodname_copilot %} for all current and future users in your organization, click **Purchase seats**.

## Granting access to {% data variables.product.prodname_copilot %} for specific users in your organization

{% ifversion ghec %}

> [!NOTE] You can automatically enable access for every member of a group in your identity provider (IdP) by synchronizing that group with a {% data variables.product.prodname_dotcom %} team, then giving that team access to {% data variables.product.prodname_copilot %}. For more information, see [AUTOTITLE](/organizations/organizing-members-into-teams/synchronizing-a-team-with-an-identity-provider-group).

{% endif %}

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.copilot.access-settings %}
1. If the **Allow this organization to assign seats** button is displayed, click this button.
1. Click **Start adding seats**.
1. To enable {% data variables.product.prodname_copilot %} for selected teams or users in your organization, select **Purchase for selected members**.
1. In the "Enable Copilot access for users and teams" dialog, click one of the two tabs.

   ![Screenshot of the "enable access for selected members" dialog.](/assets/images/help/copilot/enable-access-for-selected-members.png)

   * Click **Users and teams** to search for and add individual users or teams.

     To search for a user, type their username or full name in the search bar. If you select a user who is not currently a member of your organization, they will be invited to join your organization when you click **Continue to purchase** followed by **Purchase seats**.

   * Click **Upload CSV** to add users in bulk by uploading a CSV file.

     To add members in bulk, click **Choose CSV to upload**, and then upload a CSV file including either the username or email address for each member you want to add, separated by a comma. The file can contain a mixture of usernames and email addresses.

     > [!WARNING] When you upload a CSV file, unless you're using {% data variables.product.prodname_emus %}, {% data variables.product.prodname_copilot %} will search all users on {% data variables.product.prodname_dotcom_the_website %} for matches. If the CSV includes users who are not members of your organization, they will be invited to join your organization when you click **Continue to purchase** followed by **Purchase seats**. This warning does not apply to accounts using {% data variables.product.prodname_emus %}.

     Review the list of users generated from your CSV file. Clear the selection of any users you do not want to add.

1. Click **Continue to purchase**, then click **Purchase seats**.

## Using the API to grant access to {% data variables.product.prodname_copilot %}

You can use {% data variables.product.prodname_dotcom %}'s REST API to grant access to {% data variables.product.prodname_copilot %} for teams, or specific users, in your organization. See [Add teams to the Copilot subscription for an organization](/rest/copilot/copilot-user-management?apiVersion=2022-11-28#add-teams-to-the-copilot-subscription-for-an-organization) and [Add users to the Copilot subscription for an organization](/rest/copilot/copilot-user-management?apiVersion=2022-11-28#add-users-to-the-copilot-subscription-for-an-organization).

{% data reusables.copilot.self-serve-license-link %}

## Further reading

* [{% data variables.product.prodname_copilot %} Trust Center](https://copilot.github.trust.page)
* [AUTOTITLE](/copilot/managing-copilot/managing-github-copilot-in-your-organization/managing-github-copilot-features-in-your-organization/managing-policies-for-copilot-in-your-organization)
* [AUTOTITLE](/copilot/managing-copilot/managing-github-copilot-in-your-organization/reviewing-github-copilot-activity-in-your-organization/reviewing-usage-data-for-github-copilot-in-your-organization)
* [AUTOTITLE](/copilot/managing-copilot/managing-github-copilot-in-your-organization/managing-access-to-github-copilot-in-your-organization/revoking-access-to-copilot-for-members-of-your-organization)
