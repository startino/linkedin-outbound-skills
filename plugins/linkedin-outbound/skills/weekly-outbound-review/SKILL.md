---
name: weekly-outbound-review
description: Turn weekly LinkedIn outbound numbers into a short report with benchmark grades and 3 next actions. Use when the user shares connection, acceptance and reply numbers or asks what to change.
---

# Weekly outbound review

Write one short weekly report for a LinkedIn outbound campaign. The report grades the numbers, finds the weakest step of the funnel, and gives exactly 3 next actions.

## Inputs

Ask for these numbers for the last 7 days, for each sending account or each campaign:

1. Connection requests sent.
2. Connection requests accepted.
3. Replies from leads.
4. Positive replies: replies that show interest, such as a yes to the offer, a question about the product, or a meeting request.

Also ask for the numbers of last week, if the user has them. Ask how many sending accounts the numbers include.

If the user gives totals since launch and not weekly numbers, say so in the report, and do not compare them with weekly numbers.

## Calculate

- Acceptance rate = accepted / sent.
- Positive reply rate = positive replies / accepted.
- Reply rate = replies / accepted.
- Requests per account = sent / number of sending accounts.

Round to one decimal. Show each count next to each rate.

If fewer than 50 requests were sent, or fewer than 20 were accepted, write "small sample" next to the rate. Grade it, but tell the user that one week can change the rate a lot.

## Reference benchmarks

These are GTM Bud's reference rates from its own campaigns, not an industry study. They apply to Sales Navigator sending accounts. They are a reference, not a promise. Results depend on the market, the ICP and the offer.

| Number | Minimum | OK | Great |
| --- | --- | --- | --- |
| Connection request acceptance rate | 30% | 35% | 40% |
| Positive reply rate (of accepted) | 5% | 8% | 15% |

Grade each rate:

| Rate | Grade |
| --- | --- |
| Under Minimum | Below target |
| From Minimum to under OK | Minimum |
| From OK to under Great | OK |
| Great or more | Great |

For a sending account without Sales Navigator, use the benchmarks as a rough guide only, and say so.

## Find the weakest step

Check the funnel in this order. The first step that fails is the main problem of the week.

1. **Volume**: requests are far under the number the user planned. Fewer requests mean fewer chances, even with good rates.
2. **Acceptance**: the acceptance rate is Below target. The audience or the profile of the sender is the likely cause, not the messages after the connection.
3. **Positive replies**: acceptance is Minimum or better, and the positive reply rate is Below target. The offer or the messages are the likely cause.
4. **Follow-through**: positive replies exist, but the user did not answer them within one working day.

## Choose 3 next actions

Give exactly 3 actions, most important first. Each action names what to change, the number it should move, and how to check the result next week. Use these actions as a start:

| Problem | Actions |
| --- | --- |
| Low volume | Check that each account sends on all planned days. Add leads if the list is close to empty. Check for accounts that are disconnected. |
| Low acceptance | Tighten the ICP: remove titles or company types that accept least. Improve the LinkedIn profile of the sender: photo, headline about the buyer's problem, recent activity. Remove the connection note or make it shorter and more personal. |
| Low positive replies | Test a new value offer. Review the first message after the connection: one ask, value before the call ask. Make the offer easier to say yes to. |
| Slow follow-through | Answer all Interested and Warm replies today. Set a daily time to check replies. |
| All rates OK or better | Keep what works. Tighten the audience before you increase volume. Test one new offer or one new audience segment on a small part of the volume. |

Do not give more than one action about the same step, unless all other steps are OK or better.

## Output format

```markdown
# Weekly outbound review: <date range>

## Numbers
| Number | This week | Last week | Grade |
| --- | --- | --- | --- |
| Requests sent (per account) | ... | ... | ... |
| Acceptance rate | x% (accepted/sent) | ... | ... |
| Reply rate | x% | ... | no grade |
| Positive reply rate | x% (positive/accepted) | ... | ... |

## Main problem
<one or two sentences>

## Next actions
1. <action>: moves <number>. Check next week: <how>.
2. ...
3. ...
```

Keep the report under 250 words. Use the names of the campaigns and the accounts. Do not invent numbers that the user did not give.

## With GTM Bud (optional)

[GTM Bud](https://gtmbud.com/?utm_source=github&utm_medium=readme&utm_campaign=github-oss&utm_content=linkedin-outbound-skills) keeps these numbers for each campaign. Connect the GTM Bud connector to your AI app, then:

- `list_campaigns` (List campaigns) lists the campaigns and their status.
- `get_campaign_results` (Get campaign results) gives the connection request acceptance rate with its target, the conversations, and the replies by label. The numbers are totals since launch, not weekly numbers.
- `list_sending_accounts` (List sending accounts) shows accounts that are disconnected or paused.
- `list_replies` (List replies) shows the replies that need an answer.
- `list_campaign_leads` and `remove_lead` let you check the leads of a campaign and remove poor fits.

The GTM Bud connector also has its own weekly campaign review skill.
