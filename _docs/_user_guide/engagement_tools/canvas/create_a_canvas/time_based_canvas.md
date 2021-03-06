---
nav_title: Time-Based Functionalities for Canvas
platform: Campaigns
subplatform: Create a Canvas
page_order: .9

tools: campaigns
page_type: reference
description: "This reference article covers time-based functionalities for Canvas."
---
# Time-Based Functionalities for Canvas

> This document serves to inform you of the nuances of any time-related capabilities in Braze relating to Canvas to assist with customer questions/strategies, as well as with troubleshooting. It outlines the definition of that term or capability, the time zone it pertains to if any, an example for clarity, and other additional caveats and notes.

Canvas | Definition | Time Zone | Example | Notes |
----------------- | ---------- | --------- | ------- | ----- |
Schedule Delay<br>Send "in x day(s) at y am/pm" | Day of week + 1 calendar day + that specific time (see example) | Company's Time Zone | If a Canvas step is sent at 9pm on Monday, and the next step sends “In 1 Days at 9am”, is that going to be delivered at 9am on Tuesday or Wednesday? Answer: Tuesday at 9am. The canvas calculates the delay as Monday + 1 calendar day = Tuesday. Then it adds on the time (9am) | "Send on the next Saturday at 3:15pm" <br><br>If a user enters the canvas on a Saturday, and the first step is to "send next saturday" would be in 7 days. If they enter on a friday, "next saturday" would be in 1 day.  |
Schedule Delay<br>Send "after x day" | The 'after' clause allows the user to specify x seconds, minutes, hours and days. | Not Relevant | If canvas step is sent after 1 day, then the user will receive the step exactly 24 hours after | |
Schedule Delay with Intelligent Delivery | The behavior is the same if using in/after with Intelligent Delivery | | | Product Team is working on a solution here to either make the UI clearer or change the behavior |
Global Frequency Capping | Calendar Day | User's Timezone | I set up a frequency capping rule of send no more than 1 campaign a day<br><br>If a user receives a message at 11 pm in their local time zone, he/she can receive another message an hour later.  | We use Company's Time Zone if User's Time Zone is not Set <br><br> It's possible a user does not have to wait 24 hours to get another message, since it's based on calendar days and not a 24-hour period.|
Global Frequency Capping - Week| Rolling 7 days: now minus 7 days (now is constantly shifting) | User's Time Zone | Every 2 days will limit the capping to the previous and current calendar days in your user's local time (ending at midnight local time on the current calendar day) | |

