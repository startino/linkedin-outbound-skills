---
name: write-value-offer
description: Write 2 to 3 value offers for LinkedIn outbound: a free, useful audit, teardown, benchmark or resource for each lead, with a hook. Use when the user needs a reason to start a conversation.
---

# Write value offers for LinkedIn outbound

Write 2 to 3 value offers for one campaign. A value offer is a free and useful thing that the campaign offers to each lead. The first message names the offer and asks if the lead wants it. The call ask comes later, after the lead has received value.

A value offer is good when a lead who never buys still finds it useful.

## Inputs

Get these inputs before you write. Ask for each missing input.

1. The ICP: who the leads are, their role, their company type, their main problem. If no ICP exists, offer to run the `define-icp` skill first.
2. What the user sells, and the result that a customer gets.
3. What the user can deliver cheaply: knowledge, data, templates, past work, tools, time.
4. The format that the user prefers: a document or report, a short video, a 1-on-1 call, or no preference.
5. How much time the user can spend for each lead who says yes.

## Step 1: List the problems

Write 3 to 5 problems that the ICP has and that the user understands well. Each problem must be specific to the ICP. "Wants more revenue" is not specific. "Loses deals because proposals take a week to send" is specific.

## Step 2: Generate offer ideas

For each problem, think of offers in these types:

| Type | What the lead gets | Example |
| --- | --- | --- |
| Audit | A short review of one thing the lead owns, with 3 fixes | A review of their pricing page |
| Teardown | An analysis of a known example in their market | How a competitor gets inbound demos |
| Benchmark | How the lead compares with peers on one number | Reply times of 20 agencies like theirs |
| Short resource | A checklist, template, or guide for one task | A 1-page onboarding checklist |
| Short video | A 3 to 5 minute screen recording about their case | A walkthrough of their signup flow |

Each offer has one of two delivery modes:

- **Same for all**: one asset that each lead gets. It costs almost nothing per lead.
- **Personalized**: made for each lead after the lead says yes. It is more convincing, but it costs time per lead.

## Step 3: Score and select

Score each idea from 1 to 5 on each check. Keep the 2 or 3 ideas with the highest total.

1. **Useful alone**: the lead gets value even if they never talk to the user.
2. **Fit**: it is about a problem that the ICP has now.
3. **Low effort for the lead**: the lead only needs to say yes. No form, no call, no long input.
4. **Cheap to deliver**: a same-for-all asset, or less than 30 minutes per lead.
5. **Leads to the sale**: the offer shows the problem that the user's product solves.
6. **Credible**: the user has the knowledge or data to make it good.

Reject an offer that is a sales call with a new name, such as "a free strategy session" that is a demo. Reject an offer that the user cannot deliver within 2 working days.

## Step 4: Write each offer

For each selected offer, write:

- **Name**: 2 to 6 words that a lead understands at once.
- **What the lead gets**: one or two sentences. Name the format and the size, for example "a 1-page PDF with 5 fixes".
- **Hook**: one line for the first message. It names the offer and asks a yes or no question. It uses no hype words. Example: "I made a short checklist of the 7 checks we run before a client launches a campaign. Do you want a copy?"
  Rejected example: "We help agencies 10x their pipeline with AI. Open to a quick chat?" It names no offer, it uses hype, and it asks for a call too early.
- **Delivery plan**: the steps, the tools, and the time per lead.
- **Why it fits this ICP**: one sentence that links it to a problem from Step 1.
- **Next step after delivery**: one natural question that can lead to a conversation about the user's product.

## Output format

```markdown
# Value offers for <ICP name>

## Offer 1: <name>
- What the lead gets: ...
- Hook: "..."
- Delivery: <same for all | personalized>, <steps>, <time per lead>
- Why it fits: ...
- Next step after delivery: ...

## Offer 2: ...

## Recommendation
<Which offer to test first, and why. If there are 2 or 3 offers, suggest that the user tests them at the same time on equal parts of the audience.>
```

Show the offers to the user and ask which ones to test. Change an offer when the user says that it is too much work or does not fit.

## With GTM Bud (optional)

[GTM Bud](https://gtmbud.com/?utm_source=github&utm_medium=readme&utm_campaign=github-oss&utm_content=linkedin-outbound-skills) uses value offers in each campaign. Connect the GTM Bud connector to your AI app, then:

- `get_seller_profile` and `update_seller_profile` set the website and the LinkedIn profile that GTM Bud reads about the user.
- `get_value_offer_brief` (Get the value offer brief) gives the seller profile, the audience and the current offers of a draft campaign.
- `save_value_offers` (Save value offers) checks the offers and saves them to the draft campaign.

GTM Bud then writes the messages for each lead around the selected offers.
