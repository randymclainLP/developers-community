---
pagename: Custom Bots
redirect_from:
Keywords:
sitesection: Documents
categoryname: "Conversational AI"
documentname: Conversation Builder
subfoldername: Bots
permalink: conversation-builder-bots-custom-bots.html
indicator: both
---

### Create a custom bot

{: .important}
LivePerson recommends that —before you create a bot— you set up the [domains](intent-builder-domains.html), [intents](intent-builder-intents.html), and [entities](intent-builder-entities.html) that the bot will need. This makes creation of the bot much faster and easier because the [NLU Assist tool](conversation-builder-nlu-assist.html) can use that information along the way to suggest suitable intents and entities to use.


**To create a custom bot**
1. If you logged into Conversation Builder directly (that is, _not_ via single sign-on from LiveEngage) and you have access to multiple organizations within your LiveEngage account, verify in the upper-right corner that the organization under which the bot should exist is displayed. If the correct organization isn’t displayed, select it from the **Org Name** dropdown list.

    <img class="fancyimage" style="width:200px" src="img/ConvoBuilder/org_selection.png">

2. In the Dashboard, click **New Bot** in the upper-right corner.
3. In the dialog box that appears, select the [template](conversation-builder-templates-overview.html) on which to base the bot.
    
    The Custom Bot template uses English and includes just a Welcome dialog and a Fallback dialog (see [Dialog Types](conversation-builder-dialogs-dialog-basics.html#dialog-types)), so it’s ideal if you want to start from scratch. In this case, you’ll be prompted to enter a name and configure a few other settings before the bot is created. 

    There are also many, industry-specific, English-language templates available. If you select one of these, all settings are configured for you. We recommend that you change the bot’s name (removing the date and time stamp at a minimum) and review the other settings. For help, see [Configure bot settings](conversation-builder-bots-bot-basics.html#configure-bot-settings).

4. If you selected the Custom Bot template, in the next dialog, specify the following:

    * **Name**: Enter a name that’s concise and clear. Make sure abbreviations can be understood, and consider adding a prefix or suffix to indicate the environment (Dev, Prod, etc.) or language (En, Sp, Fr, etc.) if applicable.
    * **Description**: Enter a description that’s meaningful to you and others. Consider including language that identifies the bot's goal and key behaviors
    * **Bot Language**: This setting determines the language-specific model for LivePerson NLU; it also supports the proper rendering of left-to-right and right-to-left languages. You specify the bot language when you create the bot, and it can’t be changed afterward.
    * **Bot Group**: Optionally select the [bot group](conversation-builder-bots-bot-groups.html) for the bot. A bot can be a member of exactly one group.

5. Build out the bot, completing and adding the necessary [dialogs](conversation-builder-dialogs-dialog-basics.html) and [interactions](conversation-builder-interactions-interaction-basics.html). As you work, test the bot using the Preview tool.
6. [Save versions](conversation-builder-versions-releases.html#save-a-version) of the bot at important points in its development. This allows you to restore a version if you need.
7. [Train and tune](conversation-builder-best-practices-train-tune-nlu.html) things as you do more testing.
8. [Save a version](conversation-builder-versions-releases.html#save-a-version) of the final “Development” bot.

    At this point, you could deploy the Development bot, but LivePerson recommends that you [create a release](conversation-builder-versions-releases.html#create-a-release) copy of the bot that you deploy instead. This allows you to take live the release copy (the Production copy). Later, you can make fine-tuning changes to the Development copy as needed, without affecting the Production copy. You can then “upgrade” the Production copy accordingly.