# Deep research brief — generalised

The Week 2 market-scan prompt with the SnapLedger specifics replaced by slots.
**Brief it like an analyst on day one:** context, seeds, criteria, output contract.

```
I'm a product manager exploring [PROBLEM/OPPORTUNITY] and need a market landscape analysis.

CONTEXT: We're considering [WHAT YOU MIGHT BUILD] for [TARGET USER]. The user is
[WHO SPECIFICALLY] — not [WHO IT ISN'T]. The decision this research feeds is [DECISION].

RESEARCH TASK: Map the current market for [CATEGORY].

1. Identify the players. Start from these known ones — [SEED A], [SEED B], [SEED C] — and
   expand with any other tools active in [YEAR RANGE], especially newer AI-native entrants.
   Note which are aimed at [SEGMENT A] vs [SEGMENT B].

2. For each significant player, report: target customer and positioning; current pricing;
   [CAPABILITY DIMENSION 1]; [CAPABILITY DIMENSION 2]; integrations with [ECOSYSTEM]; and
   common user complaints from reviews and forums.

3. Market level: how is AI changing this category — what have incumbents shipped recently,
   and what are AI-native entrants doing differently? What regulation matters? What price
   bands exist, and is anyone serving [UNDERSERVED SEGMENT] well?

4. Gaps: where is the whitespace? Specifically assess whether anyone is doing
   [YOUR HYPOTHESIS].

OUTPUT: a comparison table, a short profile per player, a "how AI is changing this category"
section, and a gaps section. Cite sources throughout. Prefer recent sources and official
pricing pages. Distinguish vendor claims from user-reported experience. Flag anywhere the
evidence is thin or conflicting.
```

**Evaluate the output like a PM:** is the source real, is it recent, and would you bet a
roadmap on it? Anything you wouldn't repeat to a stakeholder, don't keep.

**Compounding run:** feed your synthesis findings back in and ask it to pressure-test the
opportunity — "the three strongest arguments this market is already served, and the three
strongest that a gap remains."
