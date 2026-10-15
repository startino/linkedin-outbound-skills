# LinkedIn Outbound Skills

LinkedIn Outbound Skills is a set of free outbound skills by [GTM Bud](https://gtmbud.com/?utm_source=github&utm_medium=readme&utm_campaign=github-oss&utm_content=linkedin-outbound-skills) for Claude, Codex and other AI assistants that read the Agent Skills format.

The skills help you plan and write LinkedIn outbound: who to contact, what to offer, what to write, how to answer replies, and what to change each week. They work without a GTM Bud account. They do not automate LinkedIn. They help you think and write.

## The skills

| Skill | What it does | You give it | You get |
| --- | --- | --- | --- |
| [`define-icp`](plugins/linkedin-outbound/skills/define-icp/SKILL.md) | Interviews you and writes an ideal customer profile | What you sell and your best customers | An ICP with must-have and nice-to-have criteria that you can check on a LinkedIn profile |
| [`write-value-offer`](plugins/linkedin-outbound/skills/write-value-offer/SKILL.md) | Writes 2 to 3 free, useful offers for each lead | Your ICP and what you can deliver | Offers such as an audit, a teardown or a benchmark, each with a one-line hook and a delivery plan |
| [`review-message-sequence`](plugins/linkedin-outbound/skills/review-message-sequence/SKILL.md) | Checks a connection note and follow-ups against a 13-point checklist | Your messages | A pass or fail for each check and a corrected sequence |
| [`triage-replies`](plugins/linkedin-outbound/skills/triage-replies/SKILL.md) | Sorts replies and drafts answers | Replies from prospects | Labels (interested, warm, not interested, wrong person, out of office) and drafts that you approve |
| [`weekly-outbound-review`](plugins/linkedin-outbound/skills/weekly-outbound-review/SKILL.md) | Grades your weekly numbers and picks 3 next actions | Requests sent, accepted, replies, positive replies | A short report against reference benchmarks |

Use the skills in this order: `define-icp`, then `write-value-offer`, then `review-message-sequence`. Use `triage-replies` and `weekly-outbound-review` each week after launch.

## Install

### Claude Code

Add this repository as a plugin marketplace, then install the plugin:

```sh
claude plugin marketplace add startino/linkedin-outbound-skills
claude plugin install linkedin-outbound@linkedin-outbound-skills
```

In a Claude Code session, you can use the same commands with a slash: `/plugin marketplace add startino/linkedin-outbound-skills` and `/plugin install linkedin-outbound@linkedin-outbound-skills`.

Claude uses a skill when your request matches it. You can also start a skill by name, for example `/linkedin-outbound:define-icp`.

Source: [Claude Code plugin marketplaces](https://code.claude.com/docs/en/plugin-marketplaces).

### Claude.ai

1. In Claude, turn on "Code execution and file creation" in Settings > Capabilities.
2. Download the folder of one skill, for example `plugins/linkedin-outbound/skills/define-icp`.
3. Make a ZIP file that has the skill folder at its root.
4. Go to Customize > Skills, select "+", then "+ Create skill", then "Upload a skill".
5. Upload the ZIP file, and turn the skill on in your skills list.

Do this once for each skill that you want. Source: [Use Skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

### Codex

Codex reads skills from `.agents/skills` in your repository and from `$HOME/.agents/skills` for all your projects. Copy the skill folders there:

```sh
git clone https://github.com/startino/linkedin-outbound-skills
mkdir -p ~/.agents/skills
cp -r linkedin-outbound-skills/plugins/linkedin-outbound/skills/* ~/.agents/skills/
```

Restart Codex if a skill does not appear. Source: [Build skills](https://learn.chatgpt.com/docs/build-skills).

## Use with GTM Bud

Each skill ends with an optional "With GTM Bud" section. [GTM Bud](https://gtmbud.com/?utm_source=github&utm_medium=readme&utm_campaign=github-oss&utm_content=linkedin-outbound-skills) runs outbound campaigns on LinkedIn: it finds leads that match your ICP, writes the messages around your value offers, and labels the replies. The [GTM Bud connector](https://github.com/startino/gtmbud-mcp) lets Claude and ChatGPT do the same steps in your GTM Bud account.

The GTM Bud trial is 14 days. It starts when you launch your first campaign, and it needs no credit card.

## Contribute

Open an issue or a pull request if a check, a benchmark or an example does not fit your market.

## License

[MIT](LICENSE)
