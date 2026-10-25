# Diagnose Search Performance
## Inputs and quality checks
Read analysis/comparison periods, timezone, market, filters, export grain, metric definitions, key event setup and site/activity changes. With only one period, describe status, not change.
Check missingness, duplicates, coverage, sampling/thresholding/export limits, channel definitions and tracking changes. Compare equivalent scopes/days; normalise per day where helpful and consider weekdays and seasonality.
Common GSC fields: date, query, page, country, device, clicks, impressions, CTR, position.
Common GA4 fields: date, landing page, session source/medium or session default channel group, device, sessions, engaged sessions, key events, purchase revenue.
Map supplied fields rather than assuming names. Do not mix session/user scopes. Users usually cannot be summed across rows.
## Metric rules
- CTR = total clicks / total impressions; engagement rate = engaged sessions / sessions; bounce rate = 1 − engagement rate. Recompute from matching numerators/denominators, not an average of row rates.
- Session key event rate = sessions with at least one key event / all sessions. Key event counts are not qualifying-session counts; do not calculate the rate without the proper numerator.
- GSC clicks differ from GA4 sessions; GA4 does not provide a complete organic-query list.
- GSC average position is not a fixed rank. Preserve source aggregation definitions rather than averaging averages across exports. Query tables can exclude anonymised queries or have limits and need not equal totals.
- GA4 engagement commonly uses a configured duration (default often 10 seconds), a key event, or two page/screen views; verify actual configuration. Bounce does not simply mean a one-page visit.
- Absolute change = current − previous; relative change = absolute change / previous; zero baseline means undefined relative change. Express rate differences in percentage points. Missing is not zero.
- Do not join GSC and GA4 rows directly by query. Before page/date comparisons, align grain, filters and URL normalisation, avoid many-to-many multiplication, and retain unmatched records. Treat systems as cross-checks, not identical populations.
## Process
1. Validate collection and comparison definitions.
2. Locate the problem along visibility → clicks → visits → engagement → business action; do not imply an exact same-user funnel.
3. Segment by supported page/query/device/country/channel dimensions.
4. Find largest absolute contributors; show denominators, small bases and uncertainty.
5. List possible explanations with evidence, counterevidence and missing checks.
6. Recommend actions, suggested owner, metric, review window and success/stop conditions.
7. Keep unconfirmed causes as hypotheses, not causal conclusions.
## Diagnostic paths
| Symptom | First checks | Possible action |
|---|---|---|
| No impressions | Indexing, crawling, demand, relevance | Fix confirmed barriers, add internal links, revisit topic |
| High impressions, low clicks | Query, position, device, live results | Improve title/value proposition based on evidence |
| More impressions, lower CTR | New lower-ranking queries and total clicks | Improve valuable new coverage |
| Fewer clicks | Impressions/position, pages, seasonality, changes | Fix supported content or technical issue |
| More visits, flat enquiries | Intent, audience, CTA, valid leads, attribution window | Improve path or decision-stage content |
| Weak engagement | Query match, opening, mobile experience, loading | Answer earlier and improve structure/experience |
| Long time, no action | Useful reading versus confusion, CTA | Investigate path; do not assume success |
| Product clicks, few purchases | Stock, price, shipping, checkout | Check barriers with commerce team |
| Stable GSC, lower GA4 | Tracking, consent, channel definitions | Explain/fix measurement before judging SEO |
| Key-event spike | Duplicate triggers, spam, business records | Verify valid leads and deduplication needs |
## Deliver
Scope/quality finding; metric comparison with bases; segment contributors; facts/hypotheses/counterevidence; checks/actions; measurement plan.
