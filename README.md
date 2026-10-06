# Chad Wallace

Applied AI engineer. I build AI tools for operating businesses: the companies that run crews, routes, bids and job sites.

## What I've built

Most of this lives in private client repositories.

- A bid-package reader used across a national contractor's regional business-development team: cited obligations, cost drivers and RFI letters.
- A field scheduler an owner and his operators use daily. It replaced route spreadsheets, a notes app and memory. Voice and photo captures from site walks go to narrow Claude specialists, and anything at 0.5 confidence or below goes to a person to confirm.
- Voice capture for English- and Spanish-speaking crews: speech-to-text with Whisper, plus spoken briefings.
- Ranked keyword search over bid documents, and a feature that keeps a quote only if it appears word for word on the source page.
- Evaluation with fixed question sets, repeated runs and per-run cost, and AI graders calibrated before they are trusted.

## Also building: AI for people, not only operations

- Wren, a Python operations agent: a chief of staff for business leaders and the staff they choose, proven first on my own install. It runs a bounded tool-calling loop with 23 tools, and its limits are enforced in code: a turn that read outside content cannot take a consequential action, outbound mail can reach only two addresses (a test attempts the violation), and one word turns it off for a person and it never turns itself back on.
- A brand and content build for a small business owner: a brand kit and logo files, a live landing page on her domain, and short clips made from the work itself. Her first content assistant was shown on one of her own posts: the model reads and offers, code checks each step, and she picks.

## How I work

I build with Claude Code as my main tool. I set the direction and approve the spec, direct the agents, and review and test what they produce.

## The tooling behind the work

I run my own engineering the way I would run AI tooling for a team:

- Checks run from hooks at every session start, so they work without anyone remembering them. Each reports clean, drift or cannot-look, and a check that cannot measure never passes as clean. I built them after agents made unreliable claims about the state of my own environment.
- Work counts only once it is proven on the live service: each session opens by checking the deployed revision against the latest commit, and one pipeline asserts the commit actually serving in production.
- In the tool that keeps my written claims true, each rule counts only after it has caught a violation planted on purpose.
- Parallel build sessions run under a watch session that builds nothing and checks what is deployed against what was merged, and an independent auditor on a different model re-checks the watch.
- AI graders are calibrated before they are trusted, and agents are evaluated on fixed test sets with cost tracked per run. One measurement removed a caching layer and roughly halved the cost.

## Public work

Public examples are being added here, starting October 2026.

Contact: linkedin.com/in/chadwallace-flowstate2026
