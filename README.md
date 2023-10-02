# whoop-re
Reverse engineering WHOOP's production API.

Production URL: `https://api.prod.whoop.com`
Development URL: `https://api.dev.whoop.com`

Needs bearer token for all requests, not sure when it expires. Use Charles or another SSL sniffing tool to find this.

# Unmapped routes
| Route      | (Guessed) Description |
| ----------- | ----------- |
| /membership      | returns member information       |
| /membership/accessories/shop/auth | returns a member-specific shop link with user's bearer token (??) |
| /activities-service/v1/cycles/aggregate   | returns range of "cycles" in a date,         |
| /rollups-service/v1/rollups/{user_id} | returns user rollups that are available on a user's profile |
| /rollups-service/v1/rollups/{user_id}?days=all | returns lifetime user's stats | 
| /home-service/v1/calendar/{key}?date={YYYY-MM-DD} | takes `recovery`, `home`, returns data based on month | 
| /home-service/v1/widget/overview | returns the home widget (strain/recovery state/hrv/strain rec |
| /coaching-service/v2/sleepneed | returns recommended times in bed for 100/85/70% need |
| /users-service/v1/stealth-mode | ???, returns `false` |
| /behavior-impact-service/v1/impact | impact journal | 
| /progression-service/v3/trends/{key} | takes `RESTORATIVE_SLEEP_PERCENT`, `TIME_IN_BED`, `HRV`, `SLEEP_DEBT_POST`, others i havent found |
| /community-service/v1/communities/featured | returns featured communities | 
| /community-service/v1/communities/{community ID}/members/details | returns membership info of a group | 
| /community-service/v1/leaderboards/communities/{community ID}/{YYYY-MM-DD}/strain/day_strain | 
