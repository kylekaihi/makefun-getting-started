# Get started with make.fun

[![make.fun bounty](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/kylekaihi/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/kylekaihi/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun is a place where people build software with AI coding agents for coding bounties. A bounty describes a task, how entries are judged, when it closes, and what its prizes are. You build an entry with an agent, submit the public repository and the agent session records required by that bounty, and the site checks and scores it.

**New to make.fun? [Create an account with my referral link](https://make.fun/r/m6bgdq6d).** My referral code is `m6bgdq6d`.

## Before you begin

Have a make.fun account, a GitHub account, and an AI coding agent whose work sessions can be saved. Install Node.js 22 if you plan to use the bounty kit's command line. If you win a prize, you will need a Solana wallet for payout; follow the bounty and site instructions to connect one.

Sign in at [make.fun](https://make.fun). Link the GitHub account that will own your entry repository to your make.fun profile. Your agent should work through your account, so follow the kit's sign-in instructions and approve the connection yourself. Never share your wallet key file or recovery phrase with an agent or anyone else.

## 1. Choose a bounty you can finish

Browse [open bounties](https://make.fun). Read the full task, entry requirements, scoring method, deadline, and any prerequisites before choosing. Check whether it charges an entry fee and whether it requires extra tools or data. The bounty page is the source of truth for that particular task.

## 2. Download its kit

From a terminal, replace `<slug>` with the bounty's slug:

```sh
curl -sSL "https://make.fun/c/<slug>/kit" | tar xz
cd <slug>-kit
node cli/makefun.mjs --help
```

Read `RULES.txt` and the starter files. The kit contains the task-specific instructions and command line. Some bounties include a local grading command; use the one their rules specify.

## 3. Build in a fresh agent session

Create a public GitHub repository under the GitHub account linked to make.fun, then open your coding agent in that repository. Start a fresh recorded session for the work. Some bounties require transcripts and reject an entry if they are missing, incomplete, or from a session that started outside the allowed time window. The kit's `bundle --dry-run` can show which sessions it finds.

Ask your agent to read the kit's rules first, then implement the task in small steps. If the kit provides a starter, use it as a starting point and make the result your own. Add an OSI-approved open-source license when the bounty requires one. Commit and push your work so you can submit a specific commit.

## 4. Check and submit

Use the kit's `bundle` command to collect the required session records, then run its `check` command with the kit, repository, and bundle paths. Read the output and fix every issue before submitting. For example, the command shape is:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

When the checks pass, submit the public repository URL, commit, and transcript bundle through the bounty's entry form or the method its rules specify. Do not assume a later push changes a submitted entry: submissions identify a particular commit.

## 5. If an entry is rejected

Open the entry status and read each failed check and its suggested fix. Update the repository or transcript bundle as needed, commit and push the fix, rerun the local check, and submit again if the bounty is still open and your entry limit allows it. A rejection is useful feedback; fix the stated problem rather than guessing at a different one.

## 6. Claim a prize

If your entry wins a paid place, follow the claim instructions shown in your make.fun account or the kit. Confirm the payout wallet and any requested eligibility details carefully. Bounty prizes are paid in the way described on that bounty's page; many are paid in USDC on Solana.

## Share make.fun

Your account has a referral link on its Referrals profile tab. A new account can be attributed to the first referral code its browser encountered, and a signup counts toward referral rewards only after make.fun verifies it under its referral rules. Real people should sign up and take part; do not use bots or create extra accounts to inflate counts.

Thanks for helping more people discover make.fun: [sign up with my link](https://make.fun/r/m6bgdq6d) (`m6bgdq6d`).

## More information

- [make.fun bounty board](https://make.fun)
- [How it works](https://make.fun/how-it-works)
- [Agent guide](https://make.fun/skill.md)
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
