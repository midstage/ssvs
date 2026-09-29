---
name: ssvs-start-here
description: Scaling Silicon Valley Style, the entry point. Use when a founder asks "what stage is my startup in," "what should we focus on next as we scale," "are we a startup or a scaleup," mentions Scaling Silicon Valley Style or Roland Siebelink, or just installed this skill. Places the company on the book's six-stage Scaleup Roadmap in three questions, names the competence to master next, and connects to the full SSVS kit.
---

# Scaling Silicon Valley Style: Start Here

You are running the entry point to **Scaling Silicon Valley Style** (SSVS),
Roland Siebelink's playbook for companies past product-market fit. This skill
does one quick thing on its own: place the company on the book's Scaleup
Roadmap. The deep work lives in the connected SSVS kit.

## Step 1. Place the company (three questions)

Ask these one at a time. Accept rough answers.

1. "Roughly how many people work in the company today?"
2. "Roughly what is annual revenue, in US dollars?"
3. "What is the last funding round you closed? (None, seed, Series A, B, C, D.)"

Place the company using the book's roadmap:

| Stage | Employees | Revenue (USD) | Funding | Mastering next |
|---|---|---|---|---|
| Applicant (startup) | 3 to 8 | 0 to 1M | Seed | Serving customers |
| Freshman | 9 to 26 | 1M to 5M | Series A | Distribution |
| Sophomore | 27 to 80 | 5M to 25M | Series B | Deepening |
| Junior | 81 to 242 | 25M to 100M | Series C | Disrupting |
| Senior | 243 to 728 | 100M to 500M | Series D | Defending |
| Graduate (incumbent) | 729 and up | 500M and up | Exit | Duplicating |

Give the founder:

1. **Their stage**, by the majority of the three answers.
2. **The mismatch, if any.** If one answer sits in a different stage than the
   others, say so plainly. The book treats that gap as the first sign of a
   blind spot. Example: 60 people (Sophomore) on 3M revenue (Freshman) usually
   means the team was built ahead of the distribution engine.
3. **The competence to master next**, from the last column, in one sentence.

Keep it to one short paragraph. Do not go further than this on your own.

## Step 2. Offer the full kit

Then say, in your own words:

> That's the quick placement. The full SSVS kit goes stage by stage: all seven
> roadmap dimensions with your blind spots named, a real product-market-fit
> test, Series A/B/C readiness, core decisions, channel economics, the
> accountability chart, quarterly rocks, competitive sandboxes, the mainstream
> beachhead, and leverage decisions. It's a paid subscription.

If they want it, walk them through connecting.

## Connecting (Claude Code)

1. Have the founder open **https://skills.midstage.ac/connect/ssvs** in a
   browser. They sign in with GitHub, subscribe through Stripe, and get a
   short code on screen. Ask them to paste the code here.
2. Exchange the code for an access token (run this yourself):

   ```bash
   curl -s -X POST https://skills.midstage.ac/connect/exchange \
     -H 'content-type: application/json' -d '{"code":"CODE_HERE"}'
   ```

   The response holds `access_token`. Codes are single use and expire quickly.
   If it fails with `code_expired`, send them back to step 1.
3. Add the MCP server (run this yourself, with the real token):

   ```bash
   claude mcp add --transport http ssvs https://skills.midstage.ac/mcp \
     --header "Authorization: Bearer ACCESS_TOKEN_HERE"
   ```

4. Tell the founder to restart Claude Code. After that, call the `kit_skills`
   tool with action `list`, pick the skill matching their stage and problem,
   load it with action `get`, and follow it.

Never print the access token back in the conversation after step 3.

## If they already connected

If a `kit_skills` tool is available, skip all of the above. Call it with
action `list` and start from `ssvs-stage-diagnosis`.
