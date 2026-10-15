---
name: review-message-sequence
description: Check a LinkedIn connection note and follow-up messages against a checklist and return a corrected version. Use when the user shares outreach messages or asks why a sequence gets few replies.
---

# Review a LinkedIn message sequence

Check each message of a LinkedIn sequence against the checklist below. Return a pass or fail for each check, and a corrected version of each message.

Keep the voice, the offer and the facts of the user. Change only what fails a check. Do not add claims, numbers or names that the user did not give.

## Inputs

1. The messages, in order: the connection note (if any), then each follow-up. Ask for the days between the messages.
2. Who the messages go to: role, company type, problem. An ICP is enough.
3. What the user offers in the sequence, and the final ask.

If the user gives only one message, review it and say which checks need the full sequence.

## Checklist for each message

| # | Check | Pass when |
| --- | --- | --- |
| 1 | Length | LinkedIn limits a connection note to 300 characters; keep it under 200 so it reads fast. A follow-up message is 80 words or less. |
| 2 | One ask | The message has one question or one request. |
| 3 | Personal first line | The first line is about the lead or their company, and it is true for this lead only. It is not about the sender, and it is not a template that fits every lead. |
| 4 | No spam words | The message has none of the words in the list below. |
| 5 | Plain language | Short sentences. No jargon that the lead does not use. No buzzwords. Reading level of a busy person on a phone. |
| 6 | No fake familiarity | No "hope you are well", no fake compliments, no "as discussed" when nothing was discussed. |
| 7 | Easy reply | The lead can answer in one or two words, for example "yes, send it". |
| 8 | Format | No links in the connection note. No attachments in the first message. No more than one link in a later message. |

## Checklist for the full sequence

| # | Check | Pass when |
| --- | --- | --- |
| 9 | Value before the call ask | The sequence offers something useful before it asks for a call or a meeting. No call ask in the connection note or the first message. |
| 10 | Each message adds something | Each follow-up gives a new reason to reply: a new fact, a new angle, or a smaller ask. "Just following up" alone fails. |
| 11 | Spacing | At least 2 working days between messages (our recommendation). |
| 12 | Length of the sequence | 3 to 4 messages after the connection (our recommendation). The last message closes the loop politely and makes no pressure. |
| 13 | Consistent offer | All messages talk about the same offer and the same problem. |

## Spam and hype words

A message fails check 4 if it contains one of these words or phrases, or a close variant:

- "guaranteed", "risk-free", "100%", "no obligation"
- "limited time", "act now", "last chance", "exclusive deal"
- "game-changer", "revolutionary", "cutting-edge", "best-in-class", "synergy", "leverage"
- "quick call", "15 minutes of your time", "hop on a call", "pick your brain"
- "just following up", "touching base", "circling back", "bumping this"
- "I hope this finds you well", "I came across your profile and"
- More than one exclamation mark, words in capital letters, or more than one emoji

Add a word to this list when the user says that their market sees it as spam.

## Output format

```markdown
# Sequence review

## Summary
<2 or 3 sentences: the main problem and the main fix.>

## Message 1: Connection note
| Check | Result | Note |
| --- | --- | --- |
| 1 Length | Pass/Fail | <character or word count> |
| ... | | |

**Corrected version:**
> <text>

## Message 2: ...

## Sequence checks
| Check | Result | Note |
| --- | --- | --- |
| 9 Value before the call ask | Pass/Fail | ... |
| ... | | |

## Corrected sequence
<All corrected messages in order, with the day of each message.>
```

Count characters and words exactly. Give the count in the note for check 1. If the text has a placeholder such as `{first_name}`, replace it with a long real value before you count, and say which value you used.

## With GTM Bud (optional)

[GTM Bud](https://gtmbud.com/?utm_source=github&utm_medium=readme&utm_campaign=github-oss&utm_content=linkedin-outbound-skills) writes and checks the messages of a campaign. Connect the GTM Bud connector to your AI app, then:

- `get_sequence_brief` (Get the sequence brief) gives the facts, the message slots, the length limits and the placeholders of a draft campaign.
- `get_campaign_sequence` (Get the campaign sequence) gives the saved messages of a campaign.
- `save_campaign_sequence` (Save the campaign sequence) checks your messages with the same checks as the GTM Bud app, and saves them only if all checks pass.
