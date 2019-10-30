# Legacy app deprecation
We're looking to deprecate legacy apps, which are apps created before May 2016 that have tight coupling between intent and entity. If your app looks like this, it applies to you:
![](https://i.imgur.com/clvobm6.png)
Context: https://medium.com/wit-ai/launching-built-in-nlp-for-messenger-and-sunsetting-bot-engine-beta-46e9038869a5.

## How to migrate your app
1. Create a new app, it will by default be in the new app format
2. An `intent` trait entity will be created for you. Each of your legacy app intents will map to an intent value in the `intent` entity. Reference: https://wit.ai/docs/recipes#categorize-the-user-intent

Legacy:
![](https://i.imgur.com/2rS01RR.png)
New:
![](https://i.imgur.com/jA2CRcm.png)

3. Free-text and keyword entities work in the same way as before, but they no longer are tied to specific intents. Reference: https://wit.ai/docs/recipes#which-entity-should-you-use
4. Start validating some samples!
