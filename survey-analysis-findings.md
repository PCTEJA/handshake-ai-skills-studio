# Developer Attitudes Toward AI Tools — computed findings (Stack Overflow Developer Survey 2026, file stack-overflow-survey-2026-ai.csv)

File: 30,903 rows, 29 columns. All numbers computed with pandas from the downloaded CSV; no guessing.
Columns: ResponseId, Age, Country, CodeMain, Employment, ICorPM, Role, YearsCode, WorkExp, OrgSize, Industry, WorkSetting, JobSat, AISelect, AIFreq_1, AIFreq_2, AIFreq_3, AIFreq_4, AIDaily, AISentiment, AITrust, AIComplex, AIWorkNext, Disruption, AIAvoid, AIToolSwitch, AIUse, AITry, KnowledgeSourceAI

## Headline
Trust is conditional on verifiability. AITrust (answered 14,304 = 46.3% of 30,903): "I trust it when I can easily verify the output" 6,872 = 48.0% of answered, 22.2% of all. Only 949 = 6.6% of answered, 3.1% of all trust it for many tasks including important work decisions. 1,754 = 12.3% do not trust it for most work tasks.

## 5 findings
1. Trust is conditional (AITrust, base 14,304): verify-conditional 6,872 (48.0%); trust many tasks but not important decisions 2,329 (16.3%); low-risk only 2,326 (16.3%); do not trust most tasks 1,754 (12.3%); trust incl. important decisions 949 (6.6%); not sure / do not use 74 (0.5%).
2. Liking is broad but not universal (AISentiment, base 14,428): favourable 8,949 (62.0% of answered, 29.0% of all 30,903) — very favourable 4,564 (31.6%), somewhat favourable 4,385 (30.4%); neutral 2,205 (15.3%); unfavourable 3,104 (21.5%) — somewhat 2,110 (14.6%), very 994 (6.9%); not sure 170 (1.2%).
3. Verification is the workflow (AIWorkNext, multi-select, base 13,162): Run it locally 10,067 (76.5% answered, 32.6% of all); Compare against codebase context 8,411 (63.9%); Inspect tests/security implications 6,977 (53.0%); Read official docs 4,998 (38.0%); Search Stack Overflow 1,601 (12.2%); Use as-is 1,265 (9.6% answered, 4.1% of all) — 90.4% of answered did NOT select use-as-is.
4. What breaks trust (Disruption, multi-select, base 13,648): Plausible but wrong code 9,452 (69.3%); Hard-to-review generated code 7,403 (54.2%); Missing context 6,724 (49.3%); Hallucinated package/config 6,161 (45.1%); Incorrect or stale internal knowledge 5,287 (38.7%); Outdated APIs 4,621 (33.9%). AIComplex (base 14,341): Good but not great 5,564 (38.8%), Very well 2,288 (16.0%) — combined good 7,852 (54.8%); Bad 2,299 (16.0%), Very poor 1,141 (8.0%) — combined bad 3,440 (24.0%).
5. Use is heavy, loyalty is thin (AIDaily base 10,877; AIToolSwitch base 13,144; AISelect base 17,464): 4+ hours/day 3,378 (31.1%), 2-4 hours 2,636 (24.2%) — 2+ hours combined 6,014 (55.3% answered, 19.5% of all). Switched tools 8,637 (65.7% answered, 28.0% of all); No 4,423 (33.7%); top switch reason better output quality 3,305 (25.1% answered). Tools used (multi-select): coding assistants 11,509 (65.9%), general-purpose chat 10,920 (62.5%), agents/automated workflows 4,582 (26.2%), internal tools 3,115 (17.8%); "I don't use AI tools" 2,907 as a single answer (16.6% answered, 9.4% of all).

## Probing
- By experience (YearsCode bands, AITrust base 13,971 with both answered): verify-conditional 0-4 yrs 416/1,012 (41.1%), 5-9 yrs 1,188/2,476 (48.0%), 10-19 yrs 2,245/4,726 (47.5%), 20+ yrs 2,907/5,757 (50.5%). Trust incl. important decisions: 0-4 yrs 80/1,012 (7.9%), 5-9 yrs 106/2,476 (4.3%), 10-19 yrs 272/4,726 (5.8%), 20+ yrs 446/5,757 (7.7%). Very favourable sentiment: 20+ yrs 37.8% vs 0-4 yrs 27.1%.
- By role (AITrust): verify-conditional AI/ML engineer 101/248 (40.7%), full-stack 1,971/4,128 (47.7%), back-end 975/2,057 (47.4%), front-end 239/502 (47.6%), Engineering manager 197/366 (53.8%). Trust incl. important: AI/ML 27/248 (10.9%) highest, manager 17/366 (4.6%) lowest. Very favourable sentiment: AI/ML 41.0%, manager 37.7%, Student 15.9% (131/826), students most neutral 22.6%.
- By daily hours (AITrust base 10,755): trust incl. important rises with hours — <1 hr not every day 15/748 (2.0%), <1 hr every day 21/1,322 (1.6%), 1-2 hrs 100/2,738 (3.7%), 2-4 hrs 184/2,597 (7.1%), 4+ hrs 569/3,350 (17.0%) — while verify-conditional falls to 39.2% at 4+ hrs (from 53.9% at <1 hr every day). Very favourable sentiment: 4+ hrs 57.4% vs <1 hr not every day 15.6%.
- By complex-task rating (AITrust base 14,273): trust incl. important 28.4% among "Very well" (646/2,273) vs 0.9% among "Very poor" (10/1,140); do-not-trust 43.1% among Very poor vs 4.9% among Very well. Perceived competence tracks trust more than role or org policy do.
- By org policy (AIUse, AITrust base 11,094): verify-conditional 41.9%-52.2% across policies; trust incl. important 2.9% where org does not use AI vs 9.7% where org measures AI use. Small effect.
- Alternative explanation tested: heavy use could explain trust, but even among "Good, but not great" complex-task raters only 239/5,542 (4.3%) trust it for important decisions — frequency alone does not create high-stakes trust; perceived competence does.

## Surprising finding
Heavy use despite low high-stakes trust: 31.1% of AIDaily respondents use AI 4+ hours/day and 55.3% use it 2+ hours/day, yet only 16.0% say AI handles complex tasks very well and only 6.6% trust it for important decisions. Developers use it constantly for work they can check, not for work they cannot.

## Recommendation
Build for verification first, not autonomy: one-click run-locally, diff against codebase context, generated tests/security checks, and cited sources. Market on output quality (the top switching reason, 3,305/13,144 = 25.1%), not on "trust us with important decisions". Target 4+ hours/day heavy users as champions; win the switch by being measurably better and easier to verify.

## Coverage / missing data — read before quoting
- AI questions were answered by only ~43-47% of 30,903: AITrust 14,304 (46.3%, missing 16,599 = 53.7%), AISentiment 14,428 (46.7%), AIComplex 14,341 (46.4%), AIWorkNext 13,162 (42.6%), Disruption 13,648 (44.2%), AIDaily 10,877 (35.2%). AISelect answered 17,464 (56.5%, missing 13,439 = 43.5%).
- None of the 2,907 "I don't use AI tools" (AISelect) respondents answered AITrust — AI findings describe AI-engaged respondents, not all developers. Always label the base, e.g. "6,872 of 14,304 who answered (22.2% of all 30,903)".
- Other heavy missing: Country 9,533 (30.8%), OrgSize 9,788 (31.7%), Industry 11,994 (38.8%), JobSat 12,027 (38.9%).
- AIFreq_1..4: answered 11,431 / 10,852 / 4,527 / 3,073. AIFreq_3 answered exactly equals the agents-users count (4,527) and AIFreq_4 exactly equals internal-tools users (3,073), so those two are conditional on tool type; AIFreq_1/2 are not labelled in the file — do not assign them to chat vs coding assistants definitively. Daily rates: AIFreq_1 8,403/11,431 (73.5%), AIFreq_2 7,162/10,852 (66.0%), AIFreq_3 2,889/4,527 (63.8%), AIFreq_4 1,487/3,073 (48.4%).
- Self-selected Stack Overflow survey, not a random sample of all developers.
