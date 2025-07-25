---
title: Asking GitHub Copilot questions in GitHub Mobile
intro: 'You can use {% data variables.copilot.copilot_mobile %} to answer general questions about software development, or specific questions about the code in a repository{% ifversion ghec %}. With {% data variables.copilot.copilot_enterprise_short %} you can also ask specific questions about a pull request, issue, or discussion{% endif %}.'
topics:
  - Copilot
  - Mobile
versions:
  feature: copilot-chat-for-mobile
shortTitle: Use Chat in Mobile
redirect_from:
  - /copilot/github-copilot-chat/using-github-copilot-chat-in-github-mobile
  - /copilot/github-copilot-chat/copilot-chat-in-github-mobile/using-github-copilot-chat-in-github-mobile
  - /copilot/github-copilot-chat/copilot-chat-in-github-mobile
  - /copilot/using-github-copilot/asking-github-copilot-questions-in-github-mobile
  - /copilot/using-github-copilot/copilot-chat/asking-github-copilot-questions-in-github-mobile
  - /copilot/how-tos/chat/asking-github-copilot-questions-in-github-mobile
  - /copilot/how-tos/chat/use-chat-in-mobile
contentType: how-tos
---

## Overview

{% data variables.copilot.copilot_chat %} is a chat interface that lets you ask and receive answers to coding-related questions in {% data variables.product.prodname_mobile %}. You can also use {% data variables.copilot.copilot_chat %} on either {% data variables.product.github %} or within a supported IDE. For information on using {% data variables.copilot.copilot_chat %} in an IDE, see [AUTOTITLE](/copilot/github-copilot-chat/copilot-chat-in-ides/using-github-copilot-chat-in-your-ide).

{% data variables.copilot.copilot_mobile_short %} can help you with a variety of coding-related tasks, like offering you code suggestions, providing natural language descriptions of a piece of code's functionality and purpose, generating unit tests for your code, and proposing fixes for bugs in your code. For more information, see [AUTOTITLE](/copilot/github-copilot-chat/copilot-chat-in-github-mobile/about-github-copilot-chat-in-github-mobile).

In {% data variables.product.prodname_mobile %}, you can use {% data variables.copilot.copilot_chat_short %} to ask:

* General software-related questions, without a particular context. See [Asking a general question about software development](#asking-a-general-question-about-software-development).
* Questions asked in the context of your project. See [Asking questions about a specific repository](#asking-exploratory-questions-about-a-repository).
* Questions about a specific file or specified lines of code within a file. See [Asking questions about specific pieces of code](#asking-questions-about-specific-pieces-of-code).{% ifversion ghec %}

With {% data variables.copilot.copilot_enterprise_short %}, you can also ask:

* Questions about a specific pull request. See [Asking questions about a specific pull request](#asking-questions-about-a-specific-pull-request).
* Questions about a specific issue. See [Asking questions about a specific issue](#asking-questions-about-a-specific-issue).
* Questions about a specific discussion. See [Asking questions about a specific discussion](#asking-questions-about-a-specific-discussion).
{% endif %}

## Limitations

The following limitations apply to {% data variables.copilot.copilot_mobile_short %}:

* The quality of the results from {% data variables.copilot.copilot_chat_short %} may, in some situations, be degraded if very large files, or a large number of files, are used as a context for a question.
* If you reach your premium request limit on mobile, {% data variables.product.prodname_copilot_short %} will automatically fall back to a free, non-premium model. Your access to premium models will reset at the start of the next billing cycle.
* If you purchased {% data variables.copilot.copilot_pro_short %} or {% data variables.copilot.copilot_pro_plus_short %} through {% data variables.product.prodname_mobile %} (via in-app purchase on iOS or Android), you cannot enable additional premium requests.

  * To enable additional premium requests, you'll need to cancel your mobile subscription and re-subscribe on {% data variables.product.prodname_dotcom_the_website %} through a web browser.
  * For help, contact {% data variables.contact.contact_support %}.

## Prerequisites

To use {% data variables.copilot.copilot_mobile_short %}, click the {% data variables.product.prodname_copilot_short %} icon in {% data variables.product.prodname_mobile %} to initiate a chat. If you don't already have an active {% data variables.product.prodname_copilot %} subscription, you will automatically get subscribed to {% data variables.copilot.copilot_free_short %}.

If you are part of an organization{% ifversion ghec %} or enterprise{% endif %} with a {% data variables.copilot.copilot_for_business %}{% ifversion ghec %} or {% data variables.copilot.copilot_enterprise %}{% endif %} subscription, the organization{% ifversion ghec %} or enterprise{% endif %} owner may need to grant you access to {% data variables.copilot.copilot_mobile_short %}. For more information, see [AUTOTITLE](/copilot/github-copilot-chat/copilot-chat-in-github-mobile/enabling-github-copilot-chat-for-github-mobile).

## Asking a general question about software development

You can ask a general question about software development{% ifversion ghec %} that is not focused on a particular context, such as a repository{% endif %}.

{% data reusables.copilot.chat-mobile-start-chat %}
1. If the page displays a previous conversation you had with {% data variables.product.prodname_copilot_short %}, tap {% octicon "kebab-horizontal" aria-label="kebab-horizontal" %} in the top right corner of the screen, and then tap **New conversation {% octicon "plus" aria-hidden="true" aria-label="plus" %}**.
1. At the bottom of the page, in the "Ask {% data variables.product.prodname_copilot_short %}" box, type a question and send the message.

   Some examples of general questions you could ask are:
   * What are the advantages of the Go programming language?
   * What is Agile software development?
   * What is the most popular JavaScript framework?
   * Give me some examples of regular expressions.
   * Write a bash script to output today's date.

1. Within a conversation thread, you can ask follow-up questions. {% data variables.product.prodname_copilot_short %} will answer within the context of the conversation. For example, you could type "tell me more" to get {% data variables.product.prodname_copilot_short %} to expand on its last comment.

   You can use your initial question as a foundation for follow-up questions. A detailed foundational prompt can help {% data variables.product.prodname_copilot_short %} provide more relevant answers to your follow-up questions. For more information, see [Prompting {% data variables.copilot.copilot_chat %} to become your personal AI assistant for accessibility](https://github.blog/2023-10-09-prompting-github-copilot-chat-to-become-your-personal-ai-assistant-for-accessibility/) on the {% data variables.product.prodname_dotcom %} Blog.

{% data reusables.copilot.chat-mobile-conversation-buttons %}

## Asking exploratory questions about a repository

You can ask questions about a specific repository, to get help with understanding the code, or to get help with a specific task you're working on.

1. In {% data variables.product.prodname_mobile %}, navigate to a repository, and tap the **{% octicon "copilot" aria-hidden="true" aria-label="copilot" %}** {% data variables.product.prodname_copilot %} icon in the bottom right corner of the screen.
1. At the bottom of the page, use the "Ask {% data variables.product.prodname_copilot_short %}" box, type a question and send the message.

   For example, if you chose the repository you are working in as the context, you could ask:

   * What is the main purpose of this repo? What problem does it solve or what functionality does it provide?
   * What web frameworks are used in this project?
   * Where is rate limiting implemented in our API?
   * How is the code organized? Explain the project architecture.
   * Are there any specific environment requirements for working on this project?

   > [!IMPORTANT]
   > {% data variables.product.prodname_copilot_short %}'s ability to answer natural language questions like these in a repository context is improved when the repository has been indexed for semantic code search. Without indexing, {% data variables.copilot.copilot_mobile_short %} may not be able to provide the most relevant answers to your questions.
   >
   > You can't trigger the creation of a semantic code search index for a repository from {% data variables.product.prodname_mobile %}. Instead you must use {% data variables.copilot.copilot_chat_short %} in a web browser. See [AUTOTITLE](/copilot/managing-copilot/managing-github-copilot-in-your-organization/managing-github-copilot-features-in-your-organization/indexing-repositories-for-copilot-chat).

{% data reusables.copilot.chat-mobile-conversation-buttons %}

## Asking questions about specific pieces of code

You can chat with {% data variables.product.prodname_copilot_short %} about a file in your repository, or about specific lines of code within a file.

1. In {% data variables.product.prodname_mobile %}, navigate to a repository and open a file.
1. Do one of the following:
   * To ask a question about the entire file, tap the {% data variables.product.prodname_copilot_short %} icon ({% octicon "copilot" aria-hidden="true" aria-label="copilot" %}) in the bottom right corner of the file view.
   * To ask a question about specific lines within the file, select and copy the lines you want to ask about. Then tap the {% data variables.product.prodname_copilot_short %} icon ({% octicon "copilot" aria-hidden="true" aria-label="copilot" %}) and paste the copied lines in the {% data variables.copilot.copilot_chat_short %} input field.

1. Type a question in the "Ask {% data variables.product.prodname_copilot_short %}" box at the bottom of the chat panel and send the message.

   For example, if you are asking about the entire file, you could enter:

   * Explain this file.
   * How could I improve this code?
   * How can I test this script?

   If you are asking about specific lines, you could enter:

   * How could I improve this class?
   * Add error handling to this code.
   * Write a unit test for this method.

   {% data variables.product.prodname_copilot_short %} responds to your request in the panel.

1. You can continue the conversation by asking a follow-up question. For example, you could type "tell me more" to get {% data variables.product.prodname_copilot_short %} to expand on its last comment.

{% ifversion ghec %}

## Asking questions about a specific pull request

You can ask questions about a specific pull request in a repository.

1. In {% data variables.product.prodname_mobile %}, navigate to a pull request in a repository, and tap the **{% octicon "copilot" aria-hidden="true" aria-label="copilot" %}** {% data variables.product.prodname_copilot %} icon in the bottom right corner of the screen.
1. At the bottom of the page, use the "Ask {% data variables.product.prodname_copilot_short %}" box, type a question and send the message.

   For example, you could ask:

   * What is the purpose of this pull request?
   * What changes are being made in this pull request?
   * Are there any potential issues with this pull request?
   * What is the status of this pull request?

   {% data variables.product.prodname_copilot_short %} responds to your request in the panel.

1. You can continue the conversation by asking a follow-up question. For example, you could type "tell me more" to get {% data variables.product.prodname_copilot_short %} to expand on its last comment.

## Asking questions about a specific issue

You can ask questions about a specific issue in a repository.

1. In {% data variables.product.prodname_mobile %}, navigate to an issue in a repository, and tap the **{% octicon "copilot" aria-hidden="true" aria-label="copilot" %}** {% data variables.product.prodname_copilot %} icon in the bottom right corner of the screen.
1. At the bottom of the page, use the "Ask {% data variables.product.prodname_copilot_short %}" box, type a question and send the message.

   For example, you could ask:

   * What is the purpose of this issue?
   * What is the status of this issue?
   * What are the steps to reproduce this issue?
   * Are there any potential solutions to this issue?

   {% data variables.product.prodname_copilot_short %} responds to your request in the panel.

1. You can continue the conversation by asking a follow-up question. For example, you could type "tell me more" to get {% data variables.product.prodname_copilot_short %} to expand on its last comment.

## Asking questions about a specific discussion

You can ask questions about a specific discussion in a repository.

1. In {% data variables.product.prodname_mobile %}, navigate to a discussion in a repository, and tap the **{% octicon "copilot" aria-hidden="true" aria-label="copilot" %}** {% data variables.product.prodname_copilot %} icon in the bottom right corner of the screen.
1. At the bottom of the page, use the "Ask {% data variables.product.prodname_copilot_short %}" box, type a question and send the message.

   For example, you could ask:

   * What is the purpose of this discussion?
   * What are the main points of this discussion?
   * What are the next steps for this discussion?
   * Are there any potential issues with this discussion?

   {% data variables.product.prodname_copilot_short %} responds to your request in the panel.

1. You can continue the conversation by asking a follow-up question. For example, you could type "tell me more" to get {% data variables.product.prodname_copilot_short %} to expand on its last comment.

{% endif %}

## Extending {% data variables.copilot.copilot_chat_short %} in {% data variables.product.prodname_mobile %}

{% data reusables.copilot.copilot-extensions.extending-copilot-chat %}

## Hiding {% data variables.copilot.copilot_chat_short %}

You can hide the floating {% data variables.product.prodname_copilot_short %} button in {% data variables.product.prodname_mobile %}.

1. In the bottom menu, tap **Profile**.
1. To view your settings, tap {% octicon "gear" aria-label="The Gear icon" %}.
1. Tap **{% data variables.product.prodname_copilot_short %}**.
1. Next to "Hide {% data variables.product.prodname_copilot_short %}", use the toggle to hide {% data variables.product.prodname_copilot_short %}.

## Sharing feedback about {% data variables.copilot.copilot_mobile %}

To give feedback about a particular {% data variables.copilot.copilot_chat_short %} response:

1. Tap the ellipsis (**...**) in the top right corner above the chat response you want to provide feedback on, and tap either **Like {% data variables.product.prodname_copilot_short %} response {% octicon "thumbsup" aria-label="The thumbs up icon" %}** or **Dislike {% data variables.product.prodname_copilot_short %} response {% octicon "thumbsdown" aria-label="The thumbs down icon" %}**,
1. Optionally, provide information about why you liked or disliked the response.
1. Tap **Submit**.
