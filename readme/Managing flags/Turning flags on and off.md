---
title: "Turning flags on and off"
excerpt: ""
---
[block:api-header]
{
  "title": "Overview"
}
[/block]
This topic explains how to enable and disable flags in the LaunchDarkly UI. 

One-click control of flag behavior is critical to nimble feature management. With LaunchDarkly, you can turn a flag on or off right from the dashboard.
[block:callout]
{
  "type": "info",
  "body": "The flag button lets you turn off a feature that's misbehaving without needing to touch any code or re-deploy your application. Wrap the entire feature in a feature flag to control or revoke its rollout seamlessly.",
  "title": "The flag button is a kill switch for any feature"
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b15dee9-Screen_Shot_2019-07-16_at_2_41_55_PM.png",
        "Screen_Shot_2019-07-16_at_2_41_55_PM.png",
        1452,
        384,
        "#f6f6f6"
      ],
      "caption": "The dashboard with two flag button called out."
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Use the button in a flag's Targeting tab",
  "body": "You can also turn a flag on or off from the flag's Targeting tab. To learn more about flag targeting, read [Targeting users](doc:targeting-users)."
}
[/block]
Flag behavior can do a lot more than just turning features on or off. Continue reading to learn more.
[block:api-header]
{
  "title": "Turning flags on"
}
[/block]
When you create a new flag, it is turned **off** by default. You can turn the flag **on** by clicking the flag button in the dashboard or the flag's Targeting tab.

To turn a flag on:
1. Navigate to the dashboard or the **Targeting** tab in the flag detail page. 
2. Click the flag button. The button turns green and displays the word **on**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/69671ce-Screen_Shot_2019-07-16_at_2.54.08_PM.png",
        "Screen Shot 2019-07-16 at 2.54.08 PM.png",
        389,
        273,
        "#f2f4f4"
      ],
      "caption": "The flag button in the Targeting tab."
    }
  ]
}
[/block]
To learn more about creating flags, read [Creating a feature flag](doc:creating-a-feature-flag).
[block:api-header]
{
  "title": "Turning flags off"
}
[/block]
When you turn a flag to **off**, you disable the targeting rules for that flag. Instead of serving an active variation, you serve the **off** variation.

In the Targeting tab, you can set an **off** variation for both boolean and multivariate flags. Boolean feature flags default to `false` when the feature flag is off. 

To turn a flag off:
1. Navigate to the dashboard or the **Targeting** tab in the flag detail page.
2. Set the kill switch to **off**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8549668-Screen_Shot_2019-07-16_at_2.31.35_PM.png",
        "Screen Shot 2019-07-16 at 2.31.35 PM.png",
        430,
        239,
        "#f2f2f2"
      ],
      "caption": "The Targeting tab with the flag turned **off**."
    }
  ]
}
[/block]
If you don't specify an explicit **off** variation, LaunchDarkly serves the fallback value for the flag, which you specified in your code's `variation` calls. This value is indicated at the bottom of the Targeting tab.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d5a5273-Screen_Shot_2019-07-16_at_2.31.44_PM.png",
        "Screen Shot 2019-07-16 at 2.31.44 PM.png",
        321,
        73,
        "#f3f4f5"
      ],
      "caption": "The fallback value at the bottom of the Targeting tab."
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Planning feature flags for future events",
  "body": "You can't schedule a flag for a particular date, but you can use targeting rules to control what it affects and when.\n\nFor example, you can serve `false` to deprecate a feature after a date of your choosing. \n\nFor more information about targeting a flag to appear before or after a date, see [Targeting users](doc:targeting-users)."
}
[/block]