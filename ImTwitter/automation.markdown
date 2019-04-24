---
layout: extra
title: Automation Rules
parent: 💾 - ImTwitter
nav_exclude: true
nav_order: 2
---
Incomplete Post
{: .label .label-red }
Chrome
{: .label .label-green }
Extension
{: .label .label-yellow }
Twitter
{: .label .label-blue }
HTML
{: .label .label-purple }
JavaScript
{: .label .label-purple }
<br>
<i>Last updated on {{ site.time | date: '%B %d, %Y' }}</i>

# Twitter Automation Rules



You can find the latest <a href="https://help.twitter.com/en/rules-and-policies/twitter-automation">Twitter automation rules</a> here. Please familiarize yourself with them to avoid being banned.

# Automation rules

_Updated November 3, 2017_

This page is primarily intended for **developers**.  

**For Twitter users:** You are ultimately responsible for the actions taken with your account, or by applications associated with your account. Before authorizing a third-party application to access or use your account, make sure you've thoroughly investigated the application and understand what it will do. If automated activity on your account violates the [Twitter Rules][1] or these automation rules, Twitter may take action on your account, including [filtering your Tweets from search results][2] or suspending your account.  

For more information on third-party applications, please see our article on [connecting and revoking third-party applications][3].  

### I. Ground Rules  

**Do!**

* Build solutions that automatically broadcast helpful information in Tweets.
* Run creative campaigns that auto-reply to users who engage with your content.
* Build solutions that automatically respond to users in Direct Messages.
* Try new things that help people (and comply with our rules).
* Make sure your application provides a good user experience and performs well — and confirm that remains the case over time.

**Don't!**

* Violate these or other policies. Be extra mindful of our rules about abuse and user privacy.
* Abuse the Twitter API or attempt to circumvent rate limits.
* Use non-API-based forms of automation, such as scripting the Twitter website. The use of these techniques may result in the permanent suspension of your account.  
* Spam or bother users, or otherwise send them unsolicited messages.

### A. The Twitter Rules and the Developer Agreement and Policy  

As with all activity on Twitter, automated activity is subject to the [Twitter Rules][1] and, if you're a developer using the Twitter API, the [Developer Agreement and Policy][4].

You should carefully review these policies to ensure that your automated activity is compliant. Automated applications or activities that violate these policies, or that facilitate or induce users to violate them, may be subject to enforcement action, potentially including suspension of associated Twitter accounts. We may also rate limit, suspend, or terminate developers' access to the Twitter API based on violations of these policies.  

Although all aspects of the Twitter Rules and the Developer Agreement and Policy apply to automated activity, you should keep the following rules top of mind:

**Spamming:** You may not send automated Tweets or Direct Messages that are spam, or otherwise engage in spamming activity. Some examples of spammy behavior to avoid with automation include:
* _Trending topics:_ You may not automatically post about trending topics on Twitter, or use automation to attempt to influence or manipulate trending topics.
* _Multiple posts/accounts:_ You may not post duplicative or substantially similar Tweets on one account or over multiple accounts you operate.

**Duplicate accounts:** You may not create and/or automate multiple accounts for duplicative or substantially similar use cases.  
* However, automating multiple accounts for related but non-duplicative use cases is permitted. For example, you may automate separate accounts to Tweet when the Hubble Space Telescope passes over different cities, such as [San Francisco][5] or [Hong Kong][6].

**Misleading links:** You may not send automated Tweets or Direct Messages containing links that are misleading, including links that maliciously or deceptively redirect through landing pages or ad pages before displaying the final content.

**Sensitive media:** Automated Tweets and Direct Messages must comply with the [Twitter media policy][7], and you should mark your account as potentially sensitive if you intend to post graphic, pornographic, or potentially sensitive media.  

**Abusive behavior:** You may not engage in any automated activity that encourages, promotes, or incites abuse, violence, hateful conduct, or harassment, on or off Twitter.  

**Private information:** You may not post private or confidential information about a person without their prior express authorization.

### B. Other Ground Rules for Automated Activity

In addition to the policies above, the following ground rules apply to all automated activity on Twitter:

* **Don't surprise or mislead users:** Automated activity should honor users' expectations. Ask for the user's permission before taking an action if you aren't sure.  
* **Mature content or profanity:** Don't Direct Message, mention, or reply to users with potentially sensitive content (including profanity), unless they've clearly indicated an intent to receive it in advance. 
* **Be thoughtful about the information you request or exchange on Twitter**
    * Tweets: Don't ask users to send you personal or private information via a public Tweet. If you need additional personal or private information from a user to provide them with customer service (or other similar use cases), you should ask the user to share such information by Direct Message or another private channel. You might even consider adding a [Direct Message deep link][8] to your Tweet.
    * Direct Messages: You should only ask users for the minimum amount of information you need to provide them with service. If you need to request or exchange particularly sensitive information (such as credit card information), you should consider directing users to your website or other appropriate channel to do so. 

### II. Activity-Specific Rules

The activity-specific rules in this section apply to taking specific automated actions on Twitter. Please read these rules carefully, as they outline both permitted and prohibited use cases of automation.

Automated applications or activities that violate these rules, or that facilitate or induce users to violate them, may be subject to enforcement action, including suspension of associated Twitter accounts. We may also rate limit, suspend, or terminate developers' access the Twitter API based on violations of these rules. As a reminder, you should also carefully review the spam guidelines in the [Twitter Rules][1] to avoid having activities performed by you, your app, or other users through your app or service flagged as spam.

### A. Automated Actions Through Another User's Account

Twitter users may authorize your app or service to [access their Twitter account through OAuth][9]. A user authorizing your app or service to access their Twitter account through OAuth does not by itself constitute sufficient consent to take automated actions through that user's account.

You may only take automated actions through another Twitter user's account if you:

* clearly describe to the user the types of automated actions that will occur;
* receive express consent from the user to take those automated actions; and
* immediately honor a user's request to opt-out of further automated actions.

If you substantially change the purpose or functionality of your app or service, you must re-obtain express consent from the user to take automated action through their account before doing so.  

These requirements apply to any automated action taken through another Twitter user's account, including posting Tweets, sending Direct Messages, deleting Tweets or Direct Messages, or following/unfollowing other accounts. For applications that offer users the ability to delete Tweets in a bulk or automated manner, you must also clearly state that Tweets are not recoverable once deleted.

### B. Automated Tweets

1\. Posting automated Tweets

**Automated Tweets that cross-post outside information:** You may post automated Tweets based on sources of outside information — such as an RSS feed, weather data, etc. — as long as you are sufficiently authorized to publish such information.

**Other automated Tweets (excluding mentions or replies):** Provided you comply with all other rules, you may post automated Tweets for entertainment, informational, or novelty purposes. As a reminder, accounts posting duplicative, spammy, or otherwise prohibited content may be subject to suspension.

2\. Posting automated mentions and replies

The reply and mention functions are intended to make communication between Twitter users easier. Automating these actions to reach many users on an unsolicited basis is an abuse of the feature, and is not permitted. For example, sending automated replies to Tweets based on keyword searches alone is not permitted. Spammy or duplicative use of mentions and replies may result in enforcement action, such as the removal of your Tweets from Search or the suspension of your app or account.  

However, you may send automated replies or mentions to Twitter users so long as:

* in advance of sending the automated reply, the recipient or mentioned user(s) have requested or have clearly indicated an intent on Twitter  to be contacted by you (i.e. opted in), for example by replying to a Tweet from your account, or by sending you a Direct Message;
* you provide a clear and easy way for such users to opt-out of receiving automated replies and mentions, and promptly honor all such opt-out requests;
* you only send one automated reply or mention per user interaction; and
* the automated reply or mention is a reply to the user's original Tweet (if your campaign is based on users posting a reply to your Tweet).

Opt-in techniques and indications of user intent take many different forms, depending on the specifics of your use case and implementation. Some examples include:

* A Tweet from your account that clearly indicates that a user taking a specific action on that Tweet (such as Retweeting it) will opt the user into receiving an automated response.
* A mention of your account by the user in a manner suggesting the user clearly wishes or intends to receive a response. If you want to run an auto-reply campaign with a campaign- or use-case-specific hashtag, users should also mention you in their Tweets.

Note that a user following your account is not on its own a sufficient indication of user intent to receive an automated response.

Additionally, we recommend that any accounts that will communicate with users via automated mentions or replies:

1. Appropriately filter responses based on potentially sensitive language in user handles, display names, and Tweet text, as well as potentially sensitive media;  

2. Check that the Tweet you are mentioning or replying to still exists (for example, using the statuses/lookup endpoint on the Twitter API).

### C. Automated Direct Messages

**Sending automated Direct Messages to users**

You may not send unsolicited Direct Messages in a bulk or automated manner, and should be thoughtful about the frequency with which you contact users via Direct Message.  

You may send automated Direct Messages to users so long as:  

* in advance of sending the Direct Message, the recipient(s) have requested or have clearly indicated an intent on Twitter to be contacted by you via Direct Message, for example by sending you a Direct Message; **_and_**  
* you provide a clear and easy way for such users to opt-out of receiving automated Direct Messages, and promptly honor all such opt-out requests.

The fact that a user is technically able to receive a Direct Message from you (e.g. because the user follows you, has enabled the ability to receive Direct Messages from any account, or because the user is in a pre-existing Direct Message conversation with you) does not necessarily mean they have requested or expect to receive automated Direct Messages from you.

**Interacting with users via Direct Message**  

Per the Ground Rules, remember to be thoughtful about the amount and type of information you request or exchange with users via Direct Messages. If you will be asking a user to provide personal or private information via an automated Direct Message, you must clearly explain how you will use the information you're collecting. Consider including a link to your privacy policy in your Direct Message to the user, as well as in your Twitter profile bio.  

Don't publicly share information received in a Direct Message conversation with a user without first obtaining explicit consent from the user. For example, if a user asks you via Direct Message about a purchase they made from you, you may not mention the user in a public Tweet that includes information about their purchase unless you have the user's explicit consent to do so.  

After a user-initiated interaction ends, don't send additional follow-up Direct Messages or mention users in a Tweet unless you get permission from the user.  

### D. Automated actions you take on Tweets or accounts  

**Automated likes:** You may not like Tweets in an automated manner.  

**Automated Retweets:** Provided you comply with all other rules, you may Retweet or Quote Tweet in an automated manner for entertainment, informational, or novelty purposes. Automated Retweets often lead to negative user experiences, and bulk, aggressive, or spammy Retweeting is a violation of the [Twitter Rules][1].  

**Automated following/unfollowing:** You may not follow or unfollow Twitter accounts in a bulk, aggressive, or indiscriminate manner. Aggressive following is a violation of the [Twitter Rules][1]. Please also review our [following rules and best practices][10] to ensure you are in compliance. Note that applications that claim to get users more followers are also prohibited under the [Twitter Rules][1].  

**Automated adding to lists or collections:** You may not add Twitter users to lists or add Tweets to collections in a bulk or indiscriminate manner. Adding a large number of unrelated users to lists is a violation of the [Twitter Rules][1].

[1]: https://help.twitter.com/en/rules-and-policies/twitter-rules
[2]: https://help.twitter.com/en/rules-and-policies/twitter-search-policies
[3]: https://help.twitter.com/en/managing-your-account/connect-or-revoke-access-to-third-party-apps.html
[4]: https://dev.twitter.com/overview/terms/agreement-and-policy
[5]: https://twitter.com/oversanfran
[6]: https://twitter.com/overhongkong
[7]: https://help.twitter.com/en/rules-and-policies/media-policy
[8]: https://business.twitter.com/en/help/campaign-editing-and-optimization/public-to-private-conversation.html
[9]: https://dev.twitter.com/oauth
[10]: https://help.twitter.com/en/rules-and-policies/twitter-following-rules


[Next Page](/ImTwitter/overview/ "Next")

