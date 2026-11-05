---
title: Observed Job List
permalink: /en/jobs/reward-mechanics/
nav_exclude: true
---

{% include en_nav.html %}

[Japanese Ver](/jobs/reward-mechanics/)


# How Job Rewards Are Determined  - Findings from Our Independent Analysis of Approximately 3,000 Jobs -

On this site, we independently analyzed 2,889 jobs to investigate the characteristics of jobs in this game and every existing job type.
This page explains the rules governing job rewards based on the findings from this independent analysis.
 > The analysis was conducted using version 0.70.64, but specifications may change in future updates.

___

## Conclusions

- (① Rewards are almost entirely determined by the route: origin > destination)
- (② For loads weighing 40 t or less, the reward is the same regardless of the cargo or weight)
- (③ For loads over 40 t, the reward is approximately 1.8 to 2 times higher; if the required level is 30, it increases by an additional 1.4 times)

___

## Scope of the Survey

| Item | Details |
|---|---|
| Game Version | ver 0.70.64 (latest version as of November 2026) |
| Departure Points | 9 locations (Frankfurt, Milan, Munich, Nancy, Nuremberg, Prague, Stuttgart, Tremola, Zurich) |
| Number of Cases | 2,889 cases (excluding duplicates, etc., from 1,031 screenshots) |
| Trailer | None |
| Base Reward | Median reward for jobs on the same route with a weight of 40 t or less and a level requirement other than 30 |

> ⚠️ Since we were able to investigate jobs in all cities without verifying the other five cities that do not have garages,
this analysis was conducted using only the nine cities with garages.
Additionally, this analysis was performed by actually launching the game rather than analyzing game files, so it cannot be ruled out that we may have missed certain special conditions or specifications. Please note that this is solely this site’s own analysis and does not constitute official information.

___

## 1. Rewards Are Largely Determined by the Route

{% comment %}
Key figures: The route alone accounts for 77.9% of reward variation; the route combined with a distance exceeding 40 t accounts for 99.3%; and at Level 30, this rises to 99.6%.
Round trips yield the same amount: In jobs with similar conditions where the starting point and destination were swapped, the average reward ratio was 1.00 (0.95–1.03).
Distance: On a per-route basis, doubling the distance results in approximately a 1.4-fold increase in reward. On the same route, a 1% increase in distance for a single trip increases the reward by approximately 0.39%.
Figure: chart_route_distance_vs_reward.png (enable the row in the image below)
Note: There are significant individual differences between routes (e.g., Stuttgart→Tübingen is 52 km and pays €2,284).
{% endcomment %}

Route alone accounts for 77.9% of the variation in rewards.
Additionally, for the same route, the reward remains the same regardless of whether it’s a one-way or round-trip.
Longer distances tend to yield higher rewards; on average, doubling the distance results in approximately a 1.4-fold increase in reward, but
the increase does not follow a strictly fixed ratio, and the multiplier varies significantly from route to route.

<!-- <img src="/assets/images/jobs/route-distance-reward.png" width="100%"> -->

___

## 2. For loads weighing 40 metric tons or less, the reward is the same regardless of the cargo

{% comment %}
Input values: Multiplier 1.00 (95% range 0.97–1.03), 2,669 cases, 61 cargo types.
Test results: Effect of cargo type (58 types): p = 0.125; correlation with weight (40 t or less): 0.03 (p = 0.42). This indicates “no significant difference was found,” not “proof that there is no difference.”
Weight Variation: 41 types of cargo with fixed weight, 28 types with variable weight (median range: 8 t).
Figure: chart_weight_vs_reward_ratio.png (For weights of 40 t or less, values cluster around 1.00)
{% endcomment %}

The vast majority fall into this group: 2,669 out of 2,889 cases—90% of the total—have exactly the same reward multiplier.
For routes under 40 t, the reward is virtually the same regardless of the cargo type or weight.
> While the amount may vary by a few percent, this is likely due to random number generation.
In this analysis, this reward multiplier is used as the baseline multiplier.

<!-- <img src="/assets/images/jobs/weight-reward-ratio.png" width="100%"> -->

___

## 3. Over 40 t: Approximately 1.8–2 times

| Weight | Multiplier | Count | Cargo |
|---|---|---|---|
| 41 t | Approx. 1.83 | 33 | Road roller |
| 42 t | Approx. 1.84 | 23 | Auto parts, generator parts |
| 45 t | Approx. 1.90 | 36 | Machinery parts, auto parts |
| 47 t | Approx. 1.95 | 38 | Auto parts, machinery parts |
| 48 t or more (11 variations) | Approx. 1.97–2.00 | 77 | Generator parts, automotive parts, machinery parts, articulated trucks, mining truck parts, wagons, cable reels |

{% comment %}
Reading: Approximately 1.83 at 41 t, rising to about 1.99 at 48 t, and then plateauing at around 2.0 thereafter (even 128 t is approximately 2.0).
Even for the same cargo type, the multiplier varies depending on weight (machinery parts, automotive parts, generator parts, cable reels).
Heavy-weight cargo accounts for 7.4% of the total (215/2,889).
Note: There is no data for exactly 40 t; the boundary lies between “40 t or less” and “41 t or more.”
{% endcomment %}

Although these jobs make up only 7.4% of the total—a small number—
there is a significant difference in pay: jobs exceeding 40 t offer approximately double the base multiplier.
Of course, the difficulty increases with the weight, but the pay is commensurate with that difficulty.
Within the group exceeding 40 t, the pay multiplier does not vary significantly.
The group exceeding 40 metric tons includes jobs with a wide range of weights, from 41 to 128 metric tons, but all fell within the 1.8–2.0x range.
___

## 4. Requirement Level 30: Approximately 1.4x More

| Weight | Multiplier | Count | Cargo |
|---|---|---|---|
| 23 t | Approx. 1.40 | 5 | Agricultural Machinery |
| 42 t | Approx. 2.59 | 4 | Heavy Cranes |
| 49 t | Approx. 2.74 | 3 | Transformers |
| 53 t | Approx. 2.81 | 1 | Mining Truck Chassis |

{% comment %}
The bonus is approximately 1.4 times (1.38–1.41 times that of a standard heavyweight of the same weight).
Note: Only 13 entries. These are listed as tentative values.
{% endcomment %}


Although this group accounted for only 0.3% of the total, it had the highest reward multiplier.
Level 30 is a tier that’s difficult to reach unless you’ve played the game for a considerable amount of time, but the rewards are correspondingly much higher.
At most, you can earn just under three times the base reward.
> Since there were only 13 instances—a job with a very low occurrence rate—there may be some margin of error in the verification results for this group.

___

## Tips for Utilization

{% comment %}
- Rewards plateau at 48 t or more (approx. 1.83 at 41 t, approx. 2.0 at 48 t or more)
- For loads of 40 t or less, the reward is the same for any job on the same route. The shorter the route, the higher the reward per 100 km (approx. €1,950 for 150 km or less, approx. €1,000 for 150–300 km, approx. €910 for 300–450 km, and approx. €850 for over 450 km)
- When choosing a job, focus on the route and weight rather than the type of cargo
{% endcomment %}

Job pay is determined by whether the load is “40 metric tons or more” and “which route” you take.
These factors are the most important when selecting a job.
Additionally, shorter jobs tend to offer higher pay per 100 km.
You should also be mindful that jobs with excessively long distances reduce your earning efficiency.

Up to 150    km: approx. €1,950
150–300   km: approx. €1,000
300–450   km: approx. €910
Over 450       km: approx. €850

___

## Research Methodology and Limitations

{% comment %}
Method: Screenshots were processed using OCR, the results from two engines were cross-checked, and rows requiring verification were confirmed via the images.
Limitations: Only 9 locations / No owned trailers / Categories with few entries (6 entries for Level 4, 13 for Level 30) / Values observed may not necessarily reflect the game’s design values / Multipliers when owning trailers will be verified separately.
{% endcomment %}

Method: Screenshots were processed using OCR, the results from two detection engines were cross-checked, and rows requiring verification were confirmed by examining the images. These are job results based on the assumption that no trailers are owned.
Limitations: Since this is not an analysis of the game files, we cannot rule out the possibility of verification errors or inaccuracies. Please use this information for reference only.
