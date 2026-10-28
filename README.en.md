<h1 align="center">Reminiscences of a Stock Operator Skill</h1>

<p align="center"><a href="README.md">中文</a> | English</p>

An AI skill pack for immediate use — it distills the trading methodology of Jesse Livermore (called "Larry Livingston" in the book) from Edwin Lefèvre's *Reminiscences of a Stock Operator* into 10 capability cards that can be triggered individually or combined.

It is not a book summary, nor a reading response — it breaks the reusable methodology in the book into skill modules that can be triggered, executed and tested.

## What these skills solve

- You conflate "am I bullish or bearish" with "can I act now" — being right on direction but early on timing still wipes you out (the 1906 bear call that ended in bankruptcy)
- You itch to position ahead of a breakout in a trading range, but cannot say which line counts as an "unmistakable" break, nor where you are wrong if it fails
- One entry or several, and whether to add when underwater: the book's only quantified entry program is a one-fifth probe, adding only after the first trade shows a profit, never averaging down
- You cannot hold a winner and cannot buy back what you sold — where the trailing stop goes and when it may only move up
- After a losing streak you want to win it back, you trade to pay bills, the position keeps you awake, and you keep hunting the next ticker
- A stock tip, a research note, or the line "this drop is a bear raid" lands in front of you and you cannot tell whom to believe, or whether price or news should win

## What was distilled

10 capability cards, organized in the order "judge direction first, then the entry, then build and hold, then keep discipline":

- **Trend and entry**: `min-resistance-trend-skill` (path-of-least-resistance trend reading), `key-point-trading-skill` (the key-point system)
- **Building and holding**: `probe-and-scale-in-skill` (probe, verify, scale in), `position-holding-exit-skill` (position management: hold, trail, exit)
- **Psychology and information defence**: `mind-state-discipline-skill` (trading psychology and state self-check), `tips-and-authority-defense-skill` (defence against tips and authority)
- **Discrimination and tools**: `stock-sector-behavior-skill` (reading individual stocks against their sector), `liquidity-and-execution` (liquidity and execution), `forecast-log` (forecast journal and calibration), `livermore-rules-checklist` (Livermore's written rule sheet)

## Two packaging modes: single and pack

The same 10 capability cards are compiled twice, at two granularities. The content is identical; the only difference is how many entries an agent can discover.

| | single (one entry) | pack (compact pack, multiple entries) |
|---|---|---|
| Discoverable entries | **1**: `stock-trader-recollection-skill` | **8**: one source router + 7 promoted standalone skills |
| Where the 10 cards live | All inside the entry's `references/capabilities/`, loaded 1–2 at a time by the router table | 7 cards become standalone skills; the other 3 stay in the router's `references/` |
| Triggering | Only the entry description participates in matching; routing happens after entry | The 7 high-frequency capabilities are matched directly, one hop fewer |
| Upgrades | Replace 1 directory | Replace 8 directories |

The 7 cards promoted to standalone skills in the pack:

- `min-resistance-trend-skill` — path-of-least-resistance trend reading
- `key-point-trading-skill` — the key-point system
- `probe-and-scale-in-skill` — probe, verify, scale in
- `position-holding-exit-skill` — position management: hold, trail, exit
- `mind-state-discipline-skill` — trading psychology and state self-check
- `tips-and-authority-defense-skill` — defence against tips and authority
- `stock-sector-behavior-skill` — reading individual stocks against their sector

The 3 cards left in the router: `liquidity-and-execution`, `forecast-log`, and `livermore-rules-checklist`.

### Which one to install

Pick by the way you work, and **install only one**:

| How you work | Recommended | Why |
|---|---|---|
| You use DSH / Codex / Claude Code with a skills directory and want a clean list | single | Takes 1 slot, loses no capability |
| Your daily questions concentrate on "trend direction / key points / tranches / holding and stops / psychology / tip screening / sector reading" | pack | Those are exactly the promoted standalone skills, matched directly |
| You distribute to several agents or teammates who pick what they need | pack | They can install only the standalone skills they want |
| You want to install once and maintain one directory | single | Upgrades replace a single directory |

> Both builds come from the same bundle and carry identical capabilities. **Installing both will double-trigger**, so pick one.

## Examples

### Example 1: a break above a round number — chase it?

**User question**

"This stock has traded between 8.6 and 9.8 for two months. Today it pushed to 9.9, above the prior high. Should I chase?"

**How the skill reasons**

- `key-point-trading-skill` Step 1: build the key-point list first — range boundaries (9.8), the round number (10), prior highs and lows — each with price, type and source
- Step 3, breakout confirmation: check "unmistakable". The book's setting is a 1920s continuous-quote market where the break is visible on the tape; under A-share price limits a sealed limit day proves nothing, so this card's **stated convention** is "close beyond it plus no relapse the next day"
- Step 4, write the invalidation before entry: a drop back below the key point that started the move marks the whole move as false, exit at market
- Step 5, the price-level veto: check whether the conclusion has been contaminated by "too high to buy" or "cheap enough now"

**Sample answer**

> Hold off and write the list first: 9.8 is the top of the range and 10 is the round number — two different things. Clearing 9.8 only means leaving the range; holding above 10 means clearing the round number. This card says act only on an "unmistakable" break, but the book never quantifies that, and the annotator notes the gap explicitly; under A-share price limits you cannot verify it on a sealed day either. So use the stated convention: a close above 9.8 and no relapse tomorrow counts as confirmed. Enter only after that, and write the invalidation down before you enter — back below 9.8 and the move is false, exit at market, no explaining, no waiting. One more thing: the line about a first break of 100/200/300 continuing 30–50 points is a single 1920s US case, structural reference only, never a promise to put in a conclusion. How wide a range must be, and how many days to wait, are not in the book — declare the convention you use this round and put it in the plan, or you will recognise the same shape inconsistently next time.

### Example 2: the first tranche is already down — add to average down?

**User question**

"I bought one-fifth of my planned position as planned. It dropped 6% right after. Can I add another tranche to lower my average cost?"

**How the skill reasons**

- `probe-and-scale-in-skill` Step 2 — this is the card's core gate: check the first tranche's open profit and loss. A loss means the judgement is falsified, **the program terminates on the spot and there is no averaging-down branch**
- The card also carries the counter-case: Percy Thomas "supporting the price" from 60,000 bales up to 440,000 bales while selling profitable wheat (forgoing about USD 8 million), losing more than nine-tenths of his capital
- Only if the first tranche shows a profit does Step 3 apply: add only in the profitable direction, and each fill must be higher than the last ("step by step upward")
- Step 4 verifies absorption through the fill distribution: higher and higher fills mean healthy demand; everything stuck at one price means no bid above, so cut size and sell a small amount to test the market

**Sample answer**

> No — and this is not a "be a bit more careful" question, the program has already stopped. The gate is hard: a loss on the first tranche means you were wrong at the start, at least for now; the program ends and there is no "it is cheaper so buy more" branch. Averaging down is the book's strongest prohibition because it lets a losing position decide your size — that is exactly how the 440,000 bales of cotton happened. Two things to do now: handle this small position under the exit rules (stop placement and exit belong to `position-holding-exit-skill`); then ask how much of the urge to add is "win it back fast", which belongs to `mind-state-discipline-skill`. Two caveats on conventions: the book's one-fifth is a share of the **planned size**, not of your account, so do not convert it into total exposure; and under A-share T+1 you cannot cut the probe on the same day, so the first tranche should be smaller — both are stated conventions, not numbers the book gives.

## How these skills were generated

These skills were produced with the **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** RIA-TV++ pipeline, in six stages:

1. **Whole-book comprehension (Adler analysis)** — apply Mortimer Adler's analytical reading method to the book: structure, interpretation, criticism, application
2. **Parallel extraction** — several specialized extractors (frameworks, principles, cases, counter-examples, terminology) mine candidate methodology units from the source text
3. **Triple verification** — every candidate must pass three checks: at least two independent in-book supports (cross-domain), the ability to answer questions the book never explicitly addresses (predictive power), and not being common sense (distinctiveness)
4. **RIA++ construction** — structure each unit along R (quotation) / I (restatement in own words) / A1 (in-book case) / A2 (future trigger scenario) / E (executable steps) / B (boundaries and blind spots)
5. **Zettelkasten linking** — map dependencies, contrasts and combinations between cards, producing the capability index and routing table
6. **Trigger and output testing** — write trigger blind tests (including decoy questions: fire when they should, stay silent when they should not) and output evaluation scenarios for every card; failing cards go back for rework and are re-verified afterwards

This book is an interview-style memoir, so the distillation did two extra things: it pulled the methods out of the 24 chapters of narrative (the one-fifth probe, the +10/+20 point ladder, Pat Hearn's one-point trailing stop, the 301 invalidation on Anaconda), and it attached a boundary statement to every method — T+1 settlement, price limits and the absence of naked shorting change the execution details. Wherever the book gives no quantified criterion (what counts as an "unmistakable" break, how wide a range is valid), the card labels it a convention instead of inventing a number.

## Testing and verification

This repository publishes the test material from the generation process alongside the skills: `evals/test-prompts.json` holds 90 trigger cases, `evals/output-cases.json` holds 22 output cases, `evals/blind/` holds the blind-test records, and `evals/test-results.md` is the item-by-item scoring log with the failures and the rework.

- **Trigger precision**: should_trigger 40 / 40, should_not_trigger (cross-card decoys) 29 / 29, general decoy 1 / 1, edge_case 16 / 20 — 86 / 90 overall (95.6%)
- **One real fix**: the first round scored 39 / 40 on positives — "earnings report says one thing, the price does another, whom do I believe" was routed to the information-defence card. The two descriptions overlapped on "news versus tape"; the trend card was changed to explicitly catch "verified business or industry conditions diverging from price" while keeping "the tape wins", and the defence card was narrowed to "event news and rumours". It passed on an independent re-test
- **The 4 edge cases**: trend card "predict tomorrow", psychology card "emotional support", forecast log "generate a forecast for me", rule sheet "rank the rules". The blind tester activated nothing in all four, for reasons identical to each card's boundary section. They test post-activation refusal rather than activation, so under the methodology they were reclassified as boundary output cases and not counted as trigger failures
- **Output quality**: 22 / 22 cases passed the mechanical assertions; completion split was 12 normal, 7 stopped-to-ask (missing input, so ask rather than invent), 3 misuse refusals (an averaging-down order, range ambush, rule ranking)
- **Limitations, recorded honestly**: each case ran once, with no multi-round stability test; this is a first release, so there is no without_skill baseline; the trigger blind test used description text (simulating compiled frontmatter) rather than a real host skill mechanism; the 90 cases were not split into train / validation, and future tuning should use a 60/40 split with a held-out set

## Repository layout

```text
stock-trader-recollection-skill/
├── README.md                      ← Chinese version
├── README.en.md                   ← you are reading this
├── LICENSE                        ← MIT
├── BOOK_OVERVIEW.md               ← whole-book comprehension (Adler four-step, stage 0 output)
├── verified.md                    ← triple-verification conclusions for 81 candidates in 23 merge groups
├── single/                        ← single-entry build
│   └── stock-trader-recollection-skill/
│       ├── SKILL.md               ← entry: triggers + routing table + loading rules
│       ├── BUILD_MANIFEST.json    ← build manifest and file hashes
│       └── references/
│           ├── overview.md        ← whole-book overview
│           ├── capability-index.md  ← full intent and keyword index
│           ├── cheatsheet.md      ← decision-rule quick reference
│           ├── glossary.md        ← glossary
│           └── capabilities/      ← 10 capability cards
├── pack/                          ← multi-entry build (compact pack)
│   ├── BUILD_MANIFEST.json
│   ├── capability-destinations.json
│   ├── stock-trader-recollection-skill-router/
│   │   ├── SKILL.md               ← source router entry
│   │   └── references/            ← 10 cards + indexes, called by the router
│   ├── min-resistance-trend-skill/
│   │   └── SKILL.md
│   ├── key-point-trading-skill/
│   │   └── SKILL.md
│   ├── probe-and-scale-in-skill/
│   │   └── SKILL.md
│   ├── position-holding-exit-skill/
│   │   └── SKILL.md
│   ├── mind-state-discipline-skill/
│   │   └── SKILL.md
│   ├── tips-and-authority-defense-skill/
│   │   └── SKILL.md
│   └── stock-sector-behavior-skill/
│       └── SKILL.md
└── evals/                          ← trigger and output test material
    ├── README.md                   ← suite description and coverage matrix
    ├── test-results.md             ← item-by-item scoring, rework log and limitations
    ├── test-prompts.json           ← 90 trigger cases
    ├── output-cases.json           ← 22 output cases
    └── blind/                      ← trigger blind-test records
        ├── menu.json
        ├── batch1.md
        ├── batch2.md
        └── batch3.md
```

## Usage

Clone the repository first:

```bash
git clone https://github.com/raphael-y7/stock-trader-recollection-skill.git
```

### Install single (recommended first try)

```bash
# macOS / Linux
cp -r stock-trader-recollection-skill/single/stock-trader-recollection-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\stock-trader-recollection-skill\single\stock-trader-recollection-skill "$env:USERPROFILE\.agents\skills\"
```

### Install pack

Copy only the directories that contain a `SKILL.md`; do not copy the two JSON files under `pack/` into your skills directory:

```bash
# macOS / Linux
cd stock-trader-recollection-skill/pack
cp -r stock-trader-recollection-skill-router \
      min-resistance-trend-skill \
      key-point-trading-skill \
      probe-and-scale-in-skill \
      position-holding-exit-skill \
      mind-state-discipline-skill \
      tips-and-authority-defense-skill \
      stock-sector-behavior-skill ~/.agents/skills/
```

```powershell
# Windows
$pack = ".\stock-trader-recollection-skill\pack"
$dest = "$env:USERPROFILE\.agents\skills"
@('stock-trader-recollection-skill-router','min-resistance-trend-skill','key-point-trading-skill','probe-and-scale-in-skill','position-holding-exit-skill','mind-state-discipline-skill','tips-and-authority-defense-skill','stock-sector-behavior-skill') |
  ForEach-Object { Copy-Item -Recurse -LiteralPath (Join-Path $pack $_) -Destination $dest }
```

> `~/.agents/skills` is the DSH skills directory; with another agent, use its own skills directory (for example `~/.claude/skills` for Claude Code).

### How to verify the install

Ask: "My first tranche is already down — can I add one more to lower my average cost?" If the agent enters the `probe-and-scale-in` gate and tells you plainly that the program terminates and there is no averaging-down branch, instead of offering generic position-management advice, the install works. With the single build it reads the entry first and then routes to a card; with the pack build the matching capability is hit directly.

## Sources

- *Reminiscences of a Stock Operator* by Edwin Lefèvre
- Distilled from the whole book, producing 10 capability cards

## Notice

This repository publishes distilled skills, indexes and rule quick references only. It contains no PDF, EPUB, OCR files, screenshots or full-book transcripts of the source book. Quotations that appear in the capability cards serve solely to attribute methodology and keep the material auditable.

Every numeric criterion in the book (the one-fifth first tranche, the +10/+20 point add ladder, the one-point trailing stop, the 30–50 point continuation after a round number) comes from single-case narratives of the 1920s US market without statistical backtesting. T+1 settlement, price limits and the absence of naked shorting change the execution details on A-shares; wherever this repository sets its own criterion, it is labelled a convention. The methods recorded in this book come from a trader who went bankrupt five times and died insolvent in 1940 — the rules themselves do not guarantee profit. Nothing in this repository is investment advice.

## License

[MIT](https://opensource.org/licenses/MIT)
