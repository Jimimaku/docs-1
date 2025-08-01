---
title: Using extensions to integrate external tools with Copilot Chat
intro: 'You can use {% data variables.copilot.copilot_extensions_short %} to interact with external tools in {% data variables.copilot.copilot_chat %}.'
product: '{% data reusables.gated-features.copilot-extensions %}'
versions:
  feature: copilot-extensions
topics:
  - Copilot
shortTitle: Use Copilot Extensions
redirect_from:
  - /copilot/github-copilot-chat/github-copilot-extensions/about-github-copilot-extensions
  - /copilot/github-copilot-chat/github-copilot-extensions/using-github-copilot-extensions
  - /copilot/github-copilot-chat/github-copilot-extensions
  - /copilot/using-github-copilot/using-extensions-to-integrate-external-tools-with-copilot-chat
  - /copilot/how-tos/context/install-copilot-extensions/using-extensions-to-integrate-external-tools-with-copilot-chat
  - /copilot/how-tos/context/install-copilot-extensions/use-copilot-extensions
contentType: how-tos
---

## About {% data variables.copilot.copilot_extensions %}

{% data reusables.copilot.copilot-extensions.copilot-extensions-intro %}

> [!NOTE] {% data variables.copilot.copilot_extensions %} are not the same as _the {% data variables.product.prodname_copilot %} extension_, which you install in your IDE to use default {% data variables.product.prodname_copilot_short %} functionality like code completion and {% data variables.copilot.copilot_chat %}. For more information on _the {% data variables.product.prodname_copilot %} extension_, see [AUTOTITLE](/copilot/managing-copilot/configure-personal-settings/installing-the-github-copilot-extension-in-your-environment).

You can get started with {% data variables.copilot.copilot_extensions_short %} in one of two ways:
* Build your own {% data variables.copilot.copilot_extension_short %}. See [AUTOTITLE](/copilot/concepts/copilot-extensions/about-copilot-extensions).
* Install a {% data variables.copilot.copilot_extension_short %} from {% data variables.product.prodname_marketplace %}.

You can interact with your custom-built or installed extension in a {% data variables.copilot.copilot_chat_short %} conversation, asking questions and performing actions that combine the capabilities of the external tool and {% data variables.product.prodname_dotcom %}. For example, if you install the Sentry extension for {% data variables.product.prodname_copilot %}, you can use the extension to get information about Sentry issues, then create and assign related tracking issues on {% data variables.product.prodname_dotcom %}.

{% data variables.copilot.copilot_extensions_short %} provide several benefits, including:

* Interaction with external tools using natural language
* Reduced context switching
* Customization of your {% data variables.copilot.copilot_chat_short %} experience for your developer flow

{% data variables.copilot.copilot_extensions_short %} are included in all {% data variables.product.prodname_copilot_short %} subscriptions.

### Supported clients and IDEs

{% data reusables.copilot.copilot-extensions.supported-clients-and-ides-table %}

## Prerequisites

**If you have a {% data variables.copilot.copilot_pro_short %} subscription**, you need to install a {% data variables.copilot.copilot_extension_short %} before you can use the extension in {% data variables.copilot.copilot_chat_short %}. See [AUTOTITLE](/copilot/github-copilot-chat/github-copilot-extensions/installing-github-copilot-extensions-for-your-personal-account).

**If you have access to {% data variables.product.prodname_copilot_short %} through a {% data variables.copilot.copilot_business_short %} or {% data variables.copilot.copilot_enterprise_short %} subscription:**
  1. An organization owner or enterprise owner needs to enable the {% data variables.copilot.copilot_extensions_short %} policy for your organization or enterprise. See [AUTOTITLE](/copilot/managing-copilot/managing-github-copilot-in-your-organization/setting-policies-for-copilot-in-your-organization/managing-policies-for-copilot-in-your-organization#setting-a-policy-for-github-copilot-extensions-in-your-organization) and [AUTOTITLE](/enterprise-cloud@latest/copilot/managing-copilot/managing-copilot-for-your-enterprise/managing-policies-and-features-for-copilot-in-your-enterprise#configuring-policies-for-github-copilot) in the {% data variables.product.prodname_ghe_cloud %} documentation.
  1. An organization owner needs to install {% data variables.copilot.copilot_extensions_short %} for your organization. See [AUTOTITLE](/copilot/github-copilot-chat/github-copilot-extensions/installing-github-copilot-extensions-for-your-organization).

## Using {% data variables.copilot.copilot_extensions %}

1. To start using a {% data variables.copilot.copilot_extension_short %}, open a supported {% data variables.copilot.copilot_chat_short %} interface. See [Supported clients and IDEs](#supported-clients-and-ides).
1. To see a list of all {% data variables.copilot.copilot_extensions_short %} available in your {% data variables.copilot.copilot_chat_short %} conversation, in the {% data variables.copilot.copilot_chat_short %} text box, type `@`.

    > [!NOTE] If you are using {% data variables.copilot.copilot_chat_short %} in an IDE, and you or your organization owner install a {% data variables.copilot.copilot_extension_short %} while your IDE is open, you need to restart your IDE to begin using the {% data variables.copilot.copilot_extension_short %}.

1. In the list of available {% data variables.copilot.copilot_extensions_short %}, click the one you want to use.
1. To begin interacting with the {% data variables.copilot.copilot_extension_short %}, in the {% data variables.copilot.copilot_chat_short %} text box, ask the extension to answer a question or perform an action, then press <kbd>Enter</kbd>. For each new request, be sure to include `@EXTENSION-NAME` at the beginning of your sentence.
    * If you did not install the {% data variables.copilot.copilot_extension_short %} yourself, and it is your first time using the {% data variables.copilot.copilot_extension_short %}, you will be asked to authorize the extension. See [AUTOTITLE](/apps/using-github-apps/authorizing-github-apps).
    * If you ask a {% data variables.copilot.copilot_extension_short %} to perform an action, you need to confirm the extension has your permission to act on your behalf before it will complete the task. After carefully reviewing the proposed action, in the confirmation dialog, click **Allow** or **Dismiss**.

## Tips for using {% data variables.copilot.copilot_extensions %}

* When you are using a {% data variables.copilot.copilot_extension_short %}, consider how you would interact with the tool outside of {% data variables.copilot.copilot_chat_short %}, then use natural language to ask questions and assign tasks that integrate the capabilities of the tool with {% data variables.product.prodname_dotcom %}. For example, [Sentry](https://sentry.io/welcome/) is an application monitoring software with a {% data variables.copilot.copilot_extension_short %}. The following are some example prompts for the Sentry extension for {% data variables.product.prodname_copilot %}:
  * `@sentry list my most recent issues`
  * `@sentry tell me more about issue ISSUE-ID-OR-ISSUE-LINK`
  * `@sentry create a {% data variables.product.prodname_dotcom %} issue for the most recent Sentry issue and assign it to @DEVELOPER`

  For information on the best ways to use a specific {% data variables.copilot.copilot_extension_short %}, read the description of the extension on [{% data variables.product.prodname_marketplace %}](https://github.com/marketplace?type=apps&copilot_app=true).
* Interactions with one {% data variables.copilot.copilot_extension_short %} will never be shared with another {% data variables.copilot.copilot_extension_short %}. To interact with different {% data variables.copilot.copilot_extensions_short %} in an IDE, change the `@EXTENSION-NAME` at the beginning of each sentence. Interactions with different extensions will appear in the same {% data variables.copilot.copilot_chat_short %} window, but the conversations themselves are automatically separated.

  {% ifversion ghec %} To interact with different {% data variables.copilot.copilot_extensions_short %} on {% data variables.product.prodname_dotcom_the_website %}, you need to start a new conversation for each extension by clicking {% octicon "plus" aria-label="New conversation" %} at the top of the {% data variables.copilot.copilot_chat_short %} window.{% endif %}

## Additional resources

For questions and issues related to {% data variables.copilot.copilot_extensions %}, please use the following resources:

* **General issues for users and builders:** Visit the [{% data variables.product.github %} Support Portal](https://support.github.com/).
* **Requests or feedback for {% data variables.product.github %}:** Use the [{% data variables.product.github %} Community Discussion Thread](https://gh.io/community-feedback).
* **Requests or feedback for third-party extension publishers:** File an issue in the [User Feedback Repo](https://github.com/copilot-extensions/user-feedback) and add a label with the extension's slug name.
* **{% data variables.product.github %} Technology Partners:** Email the partnerships team directly for assistance.
* **{% data variables.copilot.copilot_vsc_chat_participants %}:** For more information on this type of {% data variables.copilot.copilot_extension_short %}, see [Chat extensions](https://code.visualstudio.com/api/extension-guides/chat) in the {% data variables.product.prodname_vscode %} documentation.

> [!NOTE] {% data variables.contact.github_support %} is not able to answer questions regarding {% data variables.copilot.copilot_vsc_chat_participants %}, as this implementation path is owned and maintained by the {% data variables.product.prodname_vscode_shortname %} team.

## Further reading

* [AUTOTITLE](/copilot/concepts/copilot-extensions/about-copilot-extensions)
