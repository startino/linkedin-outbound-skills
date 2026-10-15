---
name: define-icp
description: Interview the user and write an ideal customer profile for LinkedIn outbound, with must-have and nice-to-have criteria you can check on a profile. Use to choose or tighten who to target.
---

# Define an ICP for LinkedIn outbound

Write one ideal customer profile (ICP) for a LinkedIn outbound campaign. The ICP tells a person or a tool which profiles to contact and which profiles to skip.

The ICP is complete when each must-have criterion is a fact that a reader can check on one LinkedIn profile or company page in less than one minute.

## Rules

- Ask questions in rounds of 3 or 4. Do not ask all questions at once.
- Use the words of the user. Do not invent customers, numbers or results.
- If the user does not know an answer, write your best estimate and mark it `(estimate)`.
- Keep one ICP for one buyer. If the user sells to two different buyers, write two ICPs.
- Do not use data that LinkedIn does not show. Revenue, tech stack and budget are not on a profile. Use a visible sign of them, or move them to signals.

## Step 1: Learn what the user sells

Ask these questions:

1. What do you sell, in one sentence?
2. Which problem does it solve, and what does that problem cost the buyer?
3. Who are your 3 best customers? Give their job titles and company names if you can.
4. Why did they buy from you and not from another option?

If the user has a website or a LinkedIn profile, ask for the link and read it before the next round.

## Step 2: Find the buyer

Ask these questions:

1. Who signs the contract or approves the spend?
2. Who feels the problem every day, if that is a different person?
3. Which job titles do these people have? Include the titles that mean the same thing in other companies.
4. Which seniority levels are too junior to buy, or too senior to reply?

Pick one primary contact. Prefer the person who feels the problem and can also approve the spend. In small companies this is often the founder or owner. In larger companies it is often a head of a function or a director.

## Step 3: Describe the company

Ask these questions:

1. What company size fits best? Use employee count ranges, for example 11 to 50.
2. Which industries or company types buy? Which do not?
3. Which countries or regions can you serve?
4. What business model fits? For example: B2B services, SaaS, ecommerce, agency, manufacturer.

## Step 4: Find signals and exclusions

A signal is a visible event or fact that makes a good fit more likely to reply now. Examples:

- The person started the role in the last 6 to 12 months.
- The company has open jobs for the role that your product supports.
- The person posted or commented about the problem in the last 90 days.
- The company raised money, opened a new office or launched a product recently.

An exclusion is a fact that removes a profile, even if all other criteria match. Ask about these exclusions:

- Competitors, partners and current customers.
- Students, interns, freelancers and job seekers, unless they are the buyer.
- Company types that cannot buy, for example government or very large enterprises.
- Industries or countries that the user cannot serve.

## Step 5: Write the criteria

Sort each requirement into one of two lists.

- **Must-have**: a profile that fails this criterion is never contacted. Use 3 to 6 must-have criteria.
- **Nice-to-have**: a profile that matches this criterion is a better fit, but a profile that fails it can still be contacted.

Write each criterion so that it passes these checks:

- It names one fact, not two.
- A reader can see the fact on the profile or the company page: title, seniority, company headcount, industry, location, time in role, recent posts.
- It has a clear yes or no answer. "Senior" is not clear. "Director, VP, Head of, or C-level title" is clear.

Too many must-have criteria make the audience too small. If the user expects fewer than about 1,000 matching people, move the weakest must-have criterion to nice-to-have. To estimate the audience size, run a LinkedIn or Sales Navigator search with the must-have filters and read the result count.

## Output format

Write the ICP in this format:

```markdown
# ICP: <short name>

**We sell:** <one sentence>
**Problem we solve:** <one sentence, with the cost to the buyer>

## Who to contact
- Titles: <list, with the equivalent titles>
- Seniority: <levels>
- Role in the purchase: <decision maker, champion, or both>

## Company
- Size: <employee range>
- Type and industry: <list>
- Location: <countries or regions>

## Must-have criteria
1. <one checkable fact>
2. ...

## Nice-to-have criteria
1. <one checkable fact>
2. ...

## Signals (reasons to reach out now)
- <signal>

## Exclusions
- <exclusion>

## Estimates and open questions
- <each item marked (estimate), and each question the user could not answer>
```

After the ICP, give the user 3 example profiles in words: one clear fit, one near miss that fails a must-have criterion, and one excluded profile. Ask the user to confirm each example. Change the criteria when the user disagrees.

## With GTM Bud (optional)

[GTM Bud](https://gtmbud.com/?utm_source=github&utm_medium=readme&utm_campaign=github-oss&utm_content=linkedin-outbound-skills) can turn this ICP into a campaign and show real people that match it. Connect the GTM Bud connector to your AI app, then:

- `create_campaign_draft` (Create a campaign draft) takes the audience description and the criteria, and checks each criterion.
- `start_prospect_preview` and `get_prospect_preview` find real LinkedIn people that match the audience.
- `get_prospect_profile` shows the full profile of one person and the result for each requirement.
- `mark_prospect_fit` records a person as a good fit or not a fit. GTM Bud keeps the mark with the campaign.
- `update_campaign_targeting` changes the audience of a draft campaign.
