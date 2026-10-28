<h1 align="center">Stock Trader Recollection Skill</h1>

<p align="center"><a href="README.md">中文</a> | English</p>

A ready-to-use AI skill toolkit — the trading methodology of Jesse Livermore, as told in Edwin Lefèvre's *Reminiscences of a Stock Operator*, distilled into 10 capability cards that can be triggered individually or combined: trend reading, entry at key points, probe-and-scale-in position building, holding and exiting a position, trading-psychology self-checks, defence against tips and authority, and distinguishing sector and single-stock behaviour.

It is not a summary of the book, and not a book review. It breaks the reusable methodology in the book into skill modules that can be triggered, executed and tested.

## What these skills solve

- You read the direction right but keep acting at the wrong spot: buying early while price is still ranging, then refusing to chase when the breakout finally comes
- When underwater you want to "average down to lower the cost", and when in profit you grab it too early — together these two moves enlarge losses and shrink gains
- A stock tip, a forwarded "small essay", a KOL call or an "insider-adjacent" piece of good news arrives, and you cannot tell whether to believe it or dodge it
- While holding a falling stock you comfort yourself with "the main force is just shaking out weak hands" / "it's a bear raid", without knowing whether the drop is legitimate or just a narrative
- Everyone in the sector is up except yours, and you want to pre-position for a catch-up; or the leader stalls and you cannot tell whether the move is over
- After a losing streak you want to win it all back at once, or you trade to make this month's bills, and only afterwards admit you were in no state to trade

## What was distilled

10 capability cards, organised as "settle direction and timing first, then position and discipline, then defend against outside information". The slugs below correspond one-to-one with the 10 capabilities in `bundle/verified.yaml` (the `-skill` suffix is part of the normalised slug):

- **Direction and timing** (2 cards): `min-resistance-trend-skill` (reading the path of least resistance), `key-point-trading-skill` (the key-point system)
- **Position-building and holding procedures** (2 cards): `probe-and-scale-in-skill` (probe, verify, then scale in), `position-holding-exit-skill` (holding, trailing and exiting a position)
- **Inner discipline and information defence** (2 cards): `mind-state-discipline-skill` (trading psychology and state self-check), `tips-and-authority-defense-skill` (defence against tips and authority)
- **Stock selection and execution** (2 cards): `stock-sector-behavior-skill` (telling sector and single-stock behaviour apart), `liquidity-and-execution-skill` (liquidity and execution)
- **Calibration and rules** (2 cards): `forecast-log-skill` (a forecast log for calibrating judgement), `livermore-rules-checklist-skill` (Livermore's written rules, as a checklist)

That is 2 + 2 + 2 + 2 + 2 = 10 cards. Seven of them are promoted to standalone entry points in the pack; three (`liquidity-and-execution-skill`, `forecast-log-skill`, `livermore-rules-checklist-skill`) are served only by the router entry — their intents are independent, but the book's evidence for them is thin or their use is infrequent, so making them standalone would only dilute trigger precision. Each card's full criteria, textual basis, book cases, trigger scenarios, executable steps and boundary blind spots live in the corresponding file under `bundle/cards/`.

## Two packaging modes: single and pack

The same 10 capability cards, compiled twice at two granularities. The content is identical; the only difference is how many entry points an agent can see.

| | single (one entry) | pack (compact pack, many entries) |
|---|---|---|
| Discoverable entries | **1**: `stock-trader-recollection-skill` | **8**: 1 source router + 7 promoted standalone skills |
| Where the 10 cards live | All under the entry's `references/capabilities/`, loaded 1–2 at a time via the routing table | The 7 promoted cards embed the whole card (all six sections R / I / A1 / A2 / E / B) in their own `SKILL.md`; the other 3 live only in the router's `references/` |
| How triggering works | Only the entry's description participates in matching; the routing table takes over once inside | The 7 high-frequency capabilities are matched directly by their descriptions — one hop fewer |
| Upgrading | Replace 1 directory | Replace 8 directories |

The 7 cards promoted to standalone skills in the pack:

- `min-resistance-trend-skill` — reading the path of least resistance
- `key-point-trading-skill` — the key-point system
- `probe-and-scale-in-skill` — probe, verify, then scale in
- `position-holding-exit-skill` — holding, trailing and exiting a position
- `mind-state-discipline-skill` — trading psychology and state self-check
- `tips-and-authority-defense-skill` — defence against tips and authority
- `stock-sector-behavior-skill` — telling sector and single-stock behaviour apart

### Which one to install

Choose by how you work — and **install only one**:

| How you work | Recommended | Why |
|---|---|---|
| You use DSH / Codex / Claude Code with a skills directory and want a clean list | single | Occupies 1 entry, with no capability missing |
| Your daily questions cluster around "can I act now / can I trust this news / should I take profit / am I in the right state" | pack | Those are exactly the promoted standalone skills, matched directly |
| You distribute to several agents or a team, each taking what they need | pack | You can install only some of the standalone skills instead of the whole set |
| You want to install once and not maintain several directories | single | Upgrading means replacing 1 directory |

> Both versions are compiled from the same bundle and carry identical capability content. **Installing both causes duplicate triggering** — install only one.

## Examples

### Example 1: ranging for a month — pre-position or wait for the breakout

**User question**

"This stock has been stuck between 12 and 13 for over a month. It's 12.6 now and looks like it wants to go up. Should I buy a bit in advance?"

**How the skill judges**

- `min-resistance-trend-skill` first: the high/low structure reads as a sideways market — a sideways market yields no directional conclusion, only the range's upper and lower limits are recorded, so "looks like it wants to go up" does not stand as a judgement
- Then `key-point-trading-skill`: build the key-point list (range top, range bottom, round numbers, prior highs and lows). The current price sits inside the range → take the stop branch "stand aside / don't touch it", and output the standby trigger prices for an upside breakout and a downside break
- Breakout confirmation is translated into A-share terms: on a limit-up day you cannot verify whether the move is real, so the agreed rule is "close beyond the level + does not fall back the next day" (**an agreed convention, not the book's wording** — the book's context was a continuous-quote market)
- Write the invalidation level down before entering: falling back below the key point the move started from means the whole move was an illusion — exit at market, no explanations, no waiting
- Check for absolute-price anchoring: the book's "first break of 100 / 200 / 300 dollars tends to run another 30–50 points" is a single 1920s US case, usable only as structural reference; "12.6 is cheaper than 13" is not a reason to buy

**Sample final answer**

> In this book's terms this is a sideways market: price has shown no clear direction for over a month, and the only correct action here is to do nothing — not "buy a little in advance", but write down the top and bottom of the range and let the market define the direction itself. So here are two standby prices: only when it breaks up through the 13 area (read together with the round number and prior highs) do we talk about buying; if it breaks down through 12, stand aside first. Don't confirm on the breakout day itself — on a limit-up day in the A-share market you cannot verify whether it is real; under the convention this repository uses, it takes "close beyond + does not fall back the next day". That rule is our translation, the book does not contain it. Before acting, write the invalidation level down: if it falls back below the key point the move started from, treat the whole move as an illusion, exit at market, and don't go looking for reasons. One last note: "12.6 is cheaper than 13" is not a reason to buy — the book has a specific veto for "too high to buy, too cheap not to buy": the absolute price is never a reason by itself.

### Example 2: a friend's "inside information" — should I buy

**User question**

"A friend at a brokerage says this company will restructure next month and told me to get in early; he says the information is solid. Should I buy?"

**How the skill judges**

- `tips-and-authority-defense-skill`, walking the four defence gates. Step one is price action first: state the current price behaviour (direction, strength versus the index and versus the sector) before any discussion of the news — reasons can be traced later, handling cannot wait
- Gate two, trend filtering: news only amplifies a trend. Good news that will not lift the price, or a bullish item that cannot push against a downtrend, is marked "caution", not "opportunity"
- Gate three, the exit-dependency chain plus the attribution / timing / behaviour triple check: who signed this? Who decides the exit later? Will that source still be present and accountable at the moment you need to sell? "A restructuring next month" has no signatory and no accountable party — the dependency chain breaks, so the tip cannot be accepted
- Gate four, attribution triage: when a decline is explained away as "the main force shaking out weak hands" or "a bear raid", the default prior is a legitimate decline (the book's "99 out of 100 cases"), and the counter-test is simple — if it really were pushed below value, buying would have stopped the fall; no bounce means it is just a narrative. The accompanying behaviour check asks what insiders actually bought or sold, which in the A-share market is visible only through periodic reports and announcements and lags, so the card requires an explicit "data unavailable" statement rather than substituting common sense
- Stop condition: an anonymous or unaccountable bullish item defaults to "not a basis for buying". If the user insists on buying, hand over to `position-holding-exit-skill` for position size and stop-loss; this card does not decide sizing

**Sample final answer**

> Treat this as a piece of information to be tested, not a reason to buy. Three questions, in order. First, is it signed and who is accountable for it? "A friend at a brokerage" is not an accountable party; a restructuring of that scale would produce an announcement, and without one it stays a rumour. Second, how will you sell? If you buy on this tip and have to wait for the same person to tell you when to sell, that chain will break exactly when you need it most — the book has a specific test for this structure, the exit-dependency chain. Third, what does the tape say? Look at the recent price action and its strength against the sector first; if the news is everywhere and the price will not rise, that in itself is the answer. So the conclusion: do not accept the tip for now, and do not build a position because of it. If you do want to participate, participate as if the tip did not exist — wait for the key-point system to give you a breakout, and use the position-management card for size and stop. One caveat: real-time insider buying and selling is not observable in the A-share market, only periodic reports, so this layer is marked "data unavailable" and will not be filled in for you.

## How these skills were generated

These skills were produced with the RIA-TV++ pipeline of **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)**, in six stages:

1. **Whole-book understanding (Adler analysis)** — Mortimer Adler's analytical reading method: structural, interpretative, critical and applied passes over the book, producing one whole-book document that serves as global context for every later extraction
2. **Parallel extraction** — several specialised extractors (frameworks, principles, cases, counter-examples, terminology) run at once to pull candidate methodology units out of the text
3. **Triple-verification screening** — every candidate must pass three checks: at least two independent supporting passages in the book (cross-domain), the power to answer questions the book never states explicitly (predictive power), and not being common sense (distinctiveness)
4. **RIA++ construction** — structured along six dimensions: R (quotation from the text), I (restatement in our own words), A1 (case from the book), A2 (future trigger scenarios), E (executable steps), B (boundaries and blind spots)
5. **Zettelkasten linking** — map the dependency, contrast and combination relations between cards, then generate the capability index and routing table
6. **Trigger and output testing** — design blind trigger tests for every card (including decoys: it must fire when it should, and stay silent when it should not) plus output evaluation scenarios; cards that fail go back for rework, then through regression testing

The nature of this particular book shaped the distillation: it is an interview-format biography, with the methodology buried in stories rather than chapter headings, so extraction proceeded segment by segment — "one concrete operation by the protagonist → the reusable criterion → the executable step". Every method also carries its 1920s US-market context (ticker tape, bucket shops, no price limits, unrestricted short selling), so every card that touches execution adds an A-share institutional translation and marks its assumptions as "agreed conventions" rather than silently inventing parameters the book never gave. The whole-book output is in `BOOK_OVERVIEW.md`, the triple-verification conclusions in `verified.md`, and the normalised definitions in `bundle/verified.yaml`.

## Testing and validation

This repository ships the test material from the generation process: `evals/` holds 90 trigger cases (`test-prompts.json`) and the item-by-item scoring record `test-results.md` — including the failures and the rework that followed, not just the passing records.

- **Trigger precision**: 90 blind-test cases, 86 / 90 (95.6%) overall. should_trigger positives 40 / 40, cross-card confusion decoys 29 / 29, general decoys 1 / 1, edge_case 16 / 20
- **One real failure, fixed**: the first round was 39 / 40 on positives — "verified fundamentals diverge from the price, which do I trust" was mis-routed to the information-defence card. Judged a skill fix: the two descriptions overlapped on "news versus tape divergence". The trend card now explicitly catches "verified business/industry situation diverging from price", and the information-defence card narrowed to "event news and rumour verification"; an independent re-test passed
- **Output quality**: 22 / 22 cases passed (each capability covered by at least one normal and one boundary-or-missing-input case), mechanical assertions 22 / 22, with the three earlier false-positive versions of the scorer checked by hand; completion modes split into 12 normal, 7 stopped-to-ask, 3 refused-misuse
- **Stop conditions**: it refuses when it should (averaging down, pre-positioning inside a range, ranking the rules) and asks when it should (missing ticker, missing key prices, missing message text) instead of forcing a conclusion
- **Limitations, stated honestly**: each case ran once, with no multi-run stability test; there is no previous-version baseline and no without-skill control group; trigger testing was based on description text rather than a real host skill mechanism; the 90 cases were not split into train / validation. Four edge cases sit on the routing-versus-output semantic boundary and were reclassified as "refusal after activation", covered by the output evaluation

## Repository structure

```text
stock-trader-recollection-skill/
├── README.md                      ← Chinese version
├── README.en.md                   ← the file you are reading
├── LICENSE                        ← MIT
├── BOOK_OVERVIEW.md               ← whole-book understanding (Adler, stage 0)
├── verified.md                    ← triple-verification results for 81 candidates, with merge groups
├── INDEX.md                       ← skill map (capability table + dependencies + loading order)
├── bundle/                        ← the card source (single source of truth for this distillation)
│   ├── verified.yaml              ← normalised definitions of the 10 capabilities (slug / criteria / destination)
│   ├── cards/                     ← 10 capability cards, filenames all ending in -skill.md
│   └── book/
│       ├── overview.md            ← whole-book overview
│       └── glossary.md            ← glossary
├── single/                        ← single-entry mode
│   └── stock-trader-recollection-skill/
│       ├── SKILL.md               ← entry: trigger conditions + routing table + loading rules
│       ├── BUILD_MANIFEST.json    ← build manifest and file hashes
│       └── references/
│           ├── overview.md        ← whole-book overview
│           ├── capability-index.md  ← full intent and keyword index
│           ├── cheatsheet.md      ← decision rules at a glance
│           ├── glossary.md        ← glossary
│           └── capabilities/      ← the 10 capability cards
├── pack/                          ← multi-entry mode (compact pack)
│   ├── BUILD_MANIFEST.json
│   ├── capability-destinations.json
│   ├── stock-trader-recollection-skill-router/
│   │   ├── SKILL.md               ← source router entry
│   │   └── references/            ← 10 cards + index / cheatsheet / glossary / overview
│   ├── min-resistance-trend-skill/
│   │   └── SKILL.md               ← a single file is the complete card
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
└── evals/                          ← test material from the generation process
    ├── test-prompts.json           ← 90 trigger cases (positives / decoys / edge)
    └── test-results.md             ← item-by-item scores, failures and rework record
```

## How to use

Clone or download the repository, then run the commands below from the repository root.

### Install single (the one to try first)

```bash
# macOS / Linux
cp -r single/stock-trader-recollection-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\single\stock-trader-recollection-skill "$env:USERPROFILE\.agents\skills\"
```

### Install pack

Copy only the directories that contain a `SKILL.md`; do not copy the two json files under `pack/` into your skills directory:

```bash
# macOS / Linux
cd pack
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
$pack = ".\pack"
$dest = "$env:USERPROFILE\.agents\skills"
@('stock-trader-recollection-skill-router','min-resistance-trend-skill','key-point-trading-skill','probe-and-scale-in-skill','position-holding-exit-skill','mind-state-discipline-skill','tips-and-authority-defense-skill','stock-sector-behavior-skill') |
  ForEach-Object { Copy-Item -Recurse -LiteralPath (Join-Path $pack $_) -Destination $dest }
```

> `~/.agents/skills` is DSH's skills directory; with another agent, use its own skills directory (Claude Code, for example, uses `~/.claude/skills`).

### How to check it is installed

Ask "this stock has been ranging for a month — can I buy now" and see whether the agent first calls it a sideways market and gives only standby trigger prices instead of "you could try a light position". With single installed, it reads the entry and then follows the routing table into a card; with pack installed, the matching capability is hit directly.

## Source

- *Reminiscences of a Stock Operator* by Edwin Lefèvre

## Disclaimer

This repository publishes only the distilled skills, indexes and rule-reference material. It contains no PDF, EPUB, OCR files, screenshots or full-book transcript of the original work. Quotations that appear inside the capability cards serve only to attribute the methodology and to keep it auditable.

All numeric criteria in the book (the 1/5 first probe, the 1:1:2 scaling ladder, the 10 / 20 point steps, the 30–50 point run after a first round-number break, "99 out of 100 cases", etc.) are case-based and experiential generalisations. The book provides no statistical backtest support for them, and most were produced under 1920s US market rules; using them in the A-share market requires translation for T+1 settlement, price limits and the absence of unrestricted short selling, together with a stated convention. Nothing in this repository constitutes investment advice.

## License

[MIT](./LICENSE)
