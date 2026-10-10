# online assessment coding practice: what the timed screen actually tests, and how to drill HackerRank and CodeSignal problems before it counts

An OA invite shows up in your inbox with almost no information. A link, a platform logo, a time limit, maybe a line about a lockdown browser. What it doesn't tell you is how hard the questions are, how the score is calculated, or whether the tab you accidentally opened will get flagged.

That gap is what most online assessment prep gets wrong. People grind hundreds of LeetCode problems, then sit a 70-minute CodeSignal assessment in a browser editor with no autocomplete and lose ten precious minutes to a syntax slip. The practice wasn't the problem. The practice didn't match the format.

So here's what the round actually looks like across the three platforms you're most likely to meet, what's worth drilling, and where a structured platform like [AlgoMonster](https://algo.monster?fpr=li69) fits — including what it does and doesn't cover.

## The online assessment is a filter, not an interview

Companies send OAs to shrink a large applicant pool before anyone spends human interview time. That single fact explains most of the format's quirks.

The screen rewards speed, correctness, and quick pattern recognition. It does not reward elegant architecture, clever naming, or a thoughtful trade-off discussion, because nobody is reading the code yet. According to a candidate guide from Ohio State's engineering career services, OAs are taken independently and early, often through HackerRank or CodeSignal, and are commonly taken with a lockdown browser so you can't reach outside resources.

For software roles, the signals are consistent:

- fluency with arrays, strings, hash maps, sets, stacks, queues, heaps, trees, graphs
- complexity awareness — knowing when an O(n²) pass will time out
- implementation discipline: empty input, duplicates, boundaries, off-by-one cases
- recovery under pressure, meaning you can use a failing test case to narrow the bug instead of rewriting the whole function
- time allocation across two to four questions

Notice what's missing: system design, behavioral depth, and any "how would this scale to a million users" follow-up. Those come later in the loop. Practising them while your OA is in three days is misallocated effort.

## HackerRank, CodeSignal, Codility: same skills, three different traps

The platform name on the invitation does change how you should prepare, mostly because scoring and test-case visibility differ. Employers configure HackerRank heavily, so a backend candidate and a frontend candidate can receive completely different experiences — coding, SQL, repository tasks, frontend projects, even code review.

|  | HackerRank | CodeSignal | Codility |
| --- | --- | --- | --- |
| Scoring | Points per passed test case; partial credit common | Certified GCA uses a 200–600 score; custom tests can differ | Test-case based; some tasks also check performance |
| Hidden tests | Often visible feedback on pass/fail | Standardised GCA structure | Little to no information on hidden cases |
| Time limit | Employer-set; commonly 70–135 minutes | GCA is normally 70 minutes, four questions | Employer-set |
| Resubmission | Usually allowed within the test | Questions can be attempted in any order | A submitted solution cannot be changed |
| Practical trap | Mixed question formats eat time you budgeted for algorithms | Four questions in 70 minutes; bonus points for fully completed ones | You may never learn whether your code was truly correct |

That CodeSignal detail matters more than most prep guides admit. Because the General Coding Assessment gives you all four questions at the start and scores module completion with bonus points for fully completed ones, hunting for the hardest-sounding problem first is usually a losing move. Pull the one you can close out cleanly, bank it, then climb.

Codility is the opposite kind of trap. A candidate-compiled guide to OA platforms notes that Codility gives you no information on hidden test cases, does not let you modify a submitted solution, and applies performance checks on some algorithmic tasks. So validation has to happen before you submit, with your own edge cases. There's no second pass.

## Practice that actually transfers to a browser editor

Three habits separate people who pass OAs from people who are technically stronger but ran out of clock.

### Drill patterns, not a problem count

Assessment prep is often framed as a volume question — 50 mediums, 100 mediums, 500. Volume helps with fluency, but the first-order skill being measured is recognition: seeing an unsorted array with a "longest subarray satisfying X" prompt and knowing that's sliding window before you type anything.

A workable priority list for OA-shaped problems:

1. Frequency maps and counting
2. Two pointers and sliding windows
3. Sorting plus a single scan
4. Stack-based parsing and monotonic stacks
5. BFS and DFS on grids, trees, and graphs
6. Binary search on arrays, and on the answer space
7. Heaps for top-k and scheduling
8. One-dimensional dynamic programming

That list isn't exhaustive — it's ordered by how often it shows up in a two-to-four-question screen. A candidate write-up of an IBM OA recorded on LeetCode's discussion board in the 2026 cycle illustrates the point: a 70-minute HackerRank test with one array-parity problem solvable by greedy simulation, and one interval-matching problem that reduces to sorting both arrays and walking them with two pointers. Neither needed an exotic algorithm. Both rewarded picking the right structure quickly.

### Read the constraints before you write the loop

The constraints section is the answer key for complexity. Rough heuristics that hold across most assessment problems:

- n up to about 100: cubic or even quartic brute force will pass
- n up to about 1,000: quadratic is usually fine
- n around 10⁵: you need O(n log n) or better
- n at 10⁶: linear time, minimal allocation

If your first idea is quadratic and n is 10⁵, don't write it and hope. It will pass the sample cases and fail the hidden ones, which is the worst possible outcome because you'll spend the rest of the clock optimising instead of moving to question two.

### Practise in the worst environment you can tolerate

This is the part most people skip. Set a timer, close every other tab, turn off autocomplete if the platform won't offer it, and use the platform's built-in editor rather than your IDE. Two or three of these sessions will surface real friction: how slow you are at reading input, which library call you always forget, how long you actually take to debug a failing custom test case.

Language choice interacts with this. Python is the fastest to write and the most readable, but it's the slowest to run — fine for most screens, occasionally fatal on tight constraints. C++ or Java closes the performance gap at the cost of boilerplate. The common advice is to use the language you can write correctly without thinking, not the one you think looks better to a reviewer, because nobody is reviewing it yet.

One more thing about the environment: employers can watch. AlgoMonster's own Amazon OA guide notes that there's no human proctor, but you're asked to photograph your ID at the start through the webcam, and browser activity is monitored — frequent tab switches can read as looking things up. Whether or not that's fair, it's the rule you're operating under.

## Free practice versus paid: what you're actually buying

You can prepare for an OA without spending money. LeetCode's free tier covers most problems, HackerRank and CodeSignal both offer practice modes that let you rehearse inside the real environment, and there are free curated lists like Blind 75 and AlgoMonster's Monster 50 that you can work through with a free account.

What you're buying with a paid platform is a reduction in decision fatigue. With three weeks and a full-time job, the bottleneck usually isn't access to problems — it's knowing which ones to do next and in what order.

That's the gap AlgoMonster targets. It teaches roughly 48 patterns with explanation, code template, and a handful of problems per pattern, plus decision flowcharts for the "which pattern is this?" step that actually decides whether you finish in time. The current Pro plan lists 500+ lessons across six courses, 1,000+ illustrations, 3,000+ editorials, unlimited AI assistant use, unlimited Speedrun, and company question banks refreshed monthly.

For assessment prep specifically, two features matter more than the rest:

**Speedrun.** It turns problems into multiple-choice questions about which technique and template applies. You don't write code, so you move through dozens of problems in the time it would take to solve two. That's a targeted drill for recognition speed, which is exactly the skill a timed screen measures. The trade-off is obvious: multiple choice builds judgement, not debugging stamina.

**Inline IDE with AI assistance.** You solve inside the browser, the way you will during the assessment, and the AI will explain a selected passage or debug a failing submission. To inspect the current setup yourself, 👉 [check the free account and plan options here](https://algo.monster?fpr=li69).

Worth knowing before you pay: AlgoMonster maintains a dedicated Amazon OA guide covering the difference between OA1 (debugging and logic), OA2 (LeetCode-style coding, typically one to two questions in about 90 minutes), and OA3 (work-style assessment with no coding). If Amazon is your target, that page alone is a free reason to create an account. You can 👉 [work through the Amazon OA question set here](https://algo.monster?fpr=li69).

## Current AlgoMonster plans and pricing

The pricing page currently lists a free tier and two paid plans. There's no month-to-month option.

| Plan | What's included | Price | Billing | Sign up |
| --- | --- | --- | --- | --- |
| Free | Limited access to sample patterns, lessons, and problems; Monster 50 and Blind 75 practice lists | $0 | — | [Start free](https://algo.monster?fpr=li69) |
| Pro — Yearly | All patterns, lessons and problems; unlimited AI assistant and Speedrun; company question banks updated monthly; 500+ lessons across 6 courses; 1,000+ illustrations; 3,000+ editorials; member discount on live bootcamps; bonus Foundation and Build an LLM courses | $99/year | Billed annually, $8.25/month effective | [Get Pro Yearly](https://algo.monster?fpr=li69) |
| Pro — Lifetime | Everything in the annual plan plus lifetime updates, one payment | $189 | Billed once | [Get Pro Lifetime](https://algo.monster?fpr=li69) |

Two pricing notes. The $99 and $189 figures are the sale prices shown on the subscribe page; a promo-tracking page that lists AlgoMonster deals puts the undiscounted rates at $198/year and $378 for lifetime, which is the 50% discount already applied at checkout. Sales on this site come and go, so the number you see on the page you land on is the one that's real. Some specialized partner content, such as the Quant Interview Prep course, is sold separately and isn't part of Pro.

The math is straightforward: a year of Pro costs less than a month of a typical interview bootcamp, and less than two-thirds of a year of LeetCode Premium at its listed $159. Lifetime at $189 pays for itself in under two renewal cycles, which matters if you expect to change jobs again in a few years — something most engineers do.

If you're still deciding, 👉 [compare the plans side by side on the pricing page](https://algo.monster?fpr=li69) rather than guessing from a review blog.

## Where AlgoMonster won't help you

Independent reviews are consistent about the limits, and they're worth taking seriously if your OA is part of a longer loop.

- **The problem bank is small.** Third-party reviewers put it around 231 lessons and problems against LeetCode's 3,000+. If you need raw volume to build fluency, this is a supplement, not a replacement. Learn patterns here, grind volume elsewhere.
- **No video.** Every explanation is text with interactive diagrams. Efficient if you learn by reading. Genuinely worse if you don't.
- **No timed interview simulation.** Final Round AI's review makes this point directly: AlgoMonster builds pattern knowledge, but it doesn't put a senior engineer on the other side of the screen asking follow-ups. Speedrun adds time pressure on recognition; it doesn't simulate the whole room.
- **System design coverage is introductory.** Fine for a phone screen, not enough for a senior loop where a dedicated design round exists.

Read those as scoping, not disqualification. For the specific job of getting through a HackerRank or CodeSignal screen in the next few weeks, a text-and-diagram pattern course with browser-based practice is a reasonable match — and the pricing reflects that it's one tool rather than the whole stack.

Nobody at the company sees your prep. They see a score. A testimonial published on AlgoMonster's site from a Meta engineer puts the emotional side of this well:

> "Failing a bunch of online assessments when you have no idea how other people are doing it is so heartbreaking."

That's the honest description of the experience. The fix is boring: know the eight patterns cold, rehearse in a browser editor, and manage the clock.

## A three-week drill plan if the OA is already on your calendar

Weeks 1–2: work through the core patterns in order, and solve two to three problems per pattern in an inline editor rather than an IDE. Track which pattern each problem used and where you lost time. Write nothing down about solutions — the goal is that the pattern becomes the first thing you notice.

Late week 2: switch to Speedrun-style recognition drills for the patterns you've covered. Twenty to thirty problems per session, no code, just technique identification. This is where you find out whether you actually recognise sliding window or merely recognise it when the topic label is visible.

Week 3: three full timed simulations. Pick one platform environment you'll plausibly face — HackerRank practice, a CodeSignal-style set, whatever the invite named — and replicate the conditions: one browser, no autocomplete, no pausing the clock. Review only the problems where you lost time rather than got stuck, because that's where the real points went.

The night before, stop. Review complexity heuristics, your language's built-in data structures, and the two-or-three-question time budget. Sleep is worth more than one more medium.

## Practical answers to the questions people actually type

**How many problems should I solve?** Enough that pattern identification is automatic across the eight core areas, which is usually 40 to 60 well-chosen problems. Past that, laddering volume without reviewing your misses produces diminishing returns.

**Is a lockdown browser always used?** No. Employers choose their integrity settings. Read the pre-test page for allowed languages, question count, and integrity requirements — it's the only reliable source for your specific invite.

**Can I use Google during the assessment?** Assume no. Even where browser monitoring doesn't involve a human, tab switches get logged, and a technical hiccup that costs you ten minutes is a bigger risk than any reference you'd find.

**Should I buy anything at all?** Only if you're stuck on sequencing rather than problem access. The free tiers on LeetCode and the assessment platforms, plus free curated lists with a free AlgoMonster account, cover a lot of ground. If you have three weeks and no idea what to study on day one, a $99 annual plan that hands you an ordered curriculum is money spent on time, which is the scarce resource here.

The assessment doesn't measure how much you've studied. It measures how fast you recognise a problem you have never seen and get working code into a browser editor before the timer ends. Practice that, in that environment, and the rest takes care of itself.
