---
title: 'The city runs on a spreadsheet'
deck: "Brackwell's building permit queue is still tracked in a shared spreadsheet fourteen years old. A 2.1 million replacement project was shelved last year after it failed to work."
standfirst: 'The city government of Brackwell processes roughly nine thousand permit applications a year through a single spreadsheet maintained by nine staff. A costly attempt to replace it with dedicated software did not survive its first month live.'
desk: 'technology'
byline: ['mira-halvorsen']
date: 2026-08-08
hero: '../../assets/sample/the-city-runs-on-a-spreadsheet.avif'
heroAlt: 'A permit office desk with a large monitor displaying a spreadsheet grid'
heroCaption: 'The Brackwell permits office tracking board, updated by hand each morning.'
heroCredit: 'Arun Pelletier / Halftone'
heroFocus: 'center'
format: 'report'
rail:
  - kind: 'stat'
    value: '14 years'
    label: 'spreadsheet in continuous use'
    source: 'Brackwell IT department'
  - kind: 'stat'
    value: '$2.1M'
    label: 'spent on the shelved replacement'
    source: 'Brackwell budget office'
  - kind: 'stat'
    value: '9'
    label: 'staff who maintain it daily'
    source: 'Brackwell permits department'
tags: ['software', 'procurement', 'infrastructure']
---

Every building permit filed in Brackwell passes, at some point, through a spreadsheet called PERMIT_TRACKER_MASTER, a file first created fourteen years ago by a clerk named Osric Vann, who retired six years into its life and left behind a document nobody since has fully rebuilt from scratch. It still runs the department.

The spreadsheet tracks roughly nine thousand applications a year across their full path: intake, zoning review, inspection scheduling and final sign-off. Nine staff update it by hand throughout the day, entering the same handful of fields so consistently that new hires are trained on the spreadsheet's conventions before they are trained on the zoning code itself. Department supervisors say they could not process a fraction of the caseload without it.

"It's ugly, it's fragile, and it works," said permits supervisor Odell Marsh, who has run the department for nine years and inherited the spreadsheet from Vann's successor. "I have had three different software vendors tell me they could replace it. Only one of them actually tried, and that one is why we're still using the spreadsheet."

## What went wrong with the replacement

In 2024 the city signed a 2.1 million contract with Aldern Systems, one of the three vendors that dominate Brackwell's software contracts, to build a dedicated permit-tracking platform intended to replace the spreadsheet entirely and add features like public-facing application status. The system went live for a pilot group of two zoning districts in March last year.

Within three weeks, permits office staff reported the new system dropping records during status updates, a bug Aldern Systems traced to a mismatch between how the software logged simultaneous edits and how the department's workflow actually required multiple staff to touch the same file in the same hour.

"We lost track of applications that people had filed months earlier," Marsh said. "That's not a bug you can live with in a permits office. People's projects were sitting in a system that had forgotten they existed."

Clerk Yusuf Adeyemi, who worked the pilot districts during the rollout before transferring to a different city department, described the weeks after launch as the worst stretch of his time in the office.

"Applicants would call asking why their permit had vanished from the online portal, and I genuinely did not have an answer," Adeyemi said. "The old spreadsheet never did that. It might be slow, it might be ugly, but it never just forgot something existed."

The scale of the problem became clear only after the fact. A post-incident review commissioned by the city and completed in June found that of roughly 1,100 applications processed through the pilot platform, 84 had at least one status update dropped entirely, and 19 had been duplicated under a second record number, creating a brief period in which the same permit appeared both approved and still pending. Untangling the duplicates took the department six weeks working alongside a data contractor hired specifically for the cleanup, at an additional cost of 40,000 that does not appear in the platform's original 2.1 million contract figure.

"The dollar number everyone quotes is the contract price," Conde said. "It doesn't include what it cost us to clean up after the contract failed. That number is smaller, but it's real, and nobody asked for it in the council session."

The department reverted to the spreadsheet within a month and the platform contract was formally shelved in a closed council session last October. The city has not sought a refund and has not announced a second attempt at replacement. Minutes from that October session, obtained through a public records request, describe the decision as a "pause pending review" rather than a cancellation, a distinction Marsh said makes little practical difference from where he sits.

"Pause or cancel, I'm not touching that system again until somebody proves to me it works," he said.

## A department that has tried this before

This was not the permits office's first attempt to leave the spreadsheet behind. An earlier project, launched in 2016 with a different, now-defunct vendor, aimed to move the department onto a general-purpose city records platform shared with three other agencies. That effort was abandoned after eighteen months when the shared platform proved unable to handle the permits office's inspection scheduling without a workaround that, in practice, meant staff kept a duplicate spreadsheet running alongside the new system anyway.

"At that point you don't have a replacement," said IT liaison Beatriz Conde, who joined the department in the aftermath of the 2016 attempt. "You have two systems and twice the work, because nobody trusted the new one enough to stop using the old one."

Conde said the 2016 experience shaped how she approached the 2024 rollout, and that she had recommended a longer parallel-running period before the department retired the spreadsheet outright. That recommendation was not followed, a decision she attributes to pressure to show results from a contract the city had already begun defending publicly before the pilot began.

"There was an announcement before there was a finished product," she said. "Once you've told the public a new system is coming, the pressure to launch it on schedule outweighs the pressure to launch it working."

## Why the spreadsheet keeps working

Marsh and Conde point to a few reasons the older system has outlasted both replacement attempts, despite looking, in Conde's words, "like something out of a filing cabinet":

- **Everyone already knows it.** No training is required for new hires beyond an afternoon with a supervisor.
- **It fails visibly.** A broken formula shows up immediately as a wrong number, rather than silently dropping a record.
- **It costs nothing extra to run.** No licensing fee, no vendor support contract, no renewal negotiation.

"None of those are reasons to never replace it," Conde said. "They're reasons the replacement has to actually be better before we retire something that, whatever its flaws, has never once lost an application."

There is a fourth reason Marsh raises less often in public meetings, because it sounds like an admission rather than a defence: the spreadsheet's very familiarity has become a kind of institutional memory. Formulas written by Vann fourteen years ago still calculate inspection deadlines correctly, encoding zoning rules that have since been amended twice, patched over rather than rebuilt by successive staff who understood the original logic well enough to extend it without fully documenting how.

One of them is column AK, which decides when an inspection is overdue. It has not been edited since 2018.

```
=IF(WEEKDAY(D2,2)>5, D2+2, D2) + VLOOKUP(G2, ZoningRules!$A$2:$B$54, 2, FALSE)
      + COUNTIFS(Holidays!$A:$A, ">="&D2, Holidays!$A:$A, "<="&D2+21)
```

"Somewhere in that file are decisions about how we count business days that nobody currently on staff could explain from scratch," Marsh said. "We just know it's been right for fourteen years. That's not a good way to run a records system. It's also not nothing."

## The vendor's side

Aldern Systems disputes that the 2024 failure reflects a broader pattern in its work for the city, pointing to other Brackwell contracts, including payroll software still in active use, that it says have run without comparable incidents. A company spokesperson said the permit platform's edit-conflict bug had since been fixed in the version Aldern Systems sells to other municipal clients, though Brackwell has not asked to test the corrected version.

"We take the Brackwell rollout seriously as a failure on our part," the spokesperson said. "We would welcome the opportunity to demonstrate the fix, whether that's here or with the next city that asks."

Marsh said he had received that offer directly and had not yet responded to it. "I believe they fixed the bug I saw. I have no way of knowing what I haven't seen yet," he said. "That's not a vendor problem specifically. That's the position anyone doing my job is in after two failed attempts."

Aldern Systems' broader record with Brackwell is not uniformly troubled. The payroll platform it built for the city's finance department has run for six years without a comparable incident, and a records system it maintains for the police department, awarded separately, has drawn no public complaints since it went live last spring. Finance director Gregor Alsvik, who oversees the payroll contract, said his department's experience with the vendor had been largely uneventful.

"I don't have a stake in the permits office's decision," Alsvik said. "What I can say is that our system has not eaten a paycheck in six years. Whatever went wrong for them, it wasn't universal to everything Aldern builds."

## What the council wants now

Council member Odalys Ferran, who also chairs the budget oversight committee reviewing the city's software contracts, has asked for a full accounting of the shelved project's costs, a request that overlaps with her office's separate inquiry into the pattern by which the same three vendors, Aldern Systems, Corvid Data and Praxil, have won the large majority of Brackwell's software work since 2019.

"Fourteen years on a spreadsheet isn't a success story," she said. "It's a warning about what happens when a replacement gets rushed to prove a budget line was worth funding, from a vendor the city keeps hiring almost by default."

| Vendor            | Awarded since 2019 |
| ----------------- | ------------------ |
| Aldern Systems    | $26.4M             |
| Corvid Data       | $18.6M             |
| Praxil            | $10.4M             |
| All other vendors | $7.6M              |

Source: Brackwell budget office, released under a public records request. Total $63.0M.

Ferran's committee has scheduled a hearing for next month at which Marsh, Conde and a representative from Aldern Systems have each been asked to appear. Marsh said he intended to bring the spreadsheet's incident log, a separate tracking file the department has kept since 2016 recording every time either replacement system dropped or duplicated a record, as evidence.

### How this was reported

Contract values and the post-incident review figures come from records released by the City of
Brackwell in response to a public records request filed in April. Aldern Systems was given ten
days to respond to each finding attributed to it. The October council session was closed; the
account of it here rests on the released minutes, not on a recording.

Marsh, for his part, has stopped waiting for a permanent fix. PERMIT_TRACKER_MASTER now backs up automatically every night, a change the department made after the 2024 incident, on the theory that if the city is going to keep running on a spreadsheet, it should at least stop losing it.
