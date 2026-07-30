# Semester Summary — Unit Meetings & Collaboration Initiative
## Kevin Lemus-Medrano | HAAG | Summer 2026

**GitHub:** [link to repo]

---

## The Starting Problem

HAAG had no formal system for cross-team collaboration. Unit meetings existed on paper but had no structure, no enforcement, and no consistency across semesters. The goal this semester was to figure out why, and build something that actually works.

---

## 1. Discovery — Understanding What Was Actually Happening

**Slack Channel Audit** (unit-level)
Reviewed message history across all active unit channels (image-processing, methods, UI) over Fall 2025 and Spring 2026. Excluded r-scripting and 3D vision, which collapsed and weren't representative of a functioning unit.

**Key findings:**
- Every unit reset scheduling from scratch every semester, no continuity
- Faculty engagement was the strongest predictor of activity, but this reflected one person's effort, not a good system
- New members frequently didn't understand what the unit was for
- Unit manager turnover disrupted multiple units mid-semester

**Project Channel Audit** (cross-check)
Scanned active project channels to find any organic collaboration patterns worth learning from. Found a small number of channels with real activity, all of which had one person voluntarily adding structure, a tracker, a bot, a consistent summary format, that wasn't required by anyone.

**Conclusion:** Successful collaboration was never a property of the system. It was individuals compensating for the system's absence. This became the core justification for everything built afterward.

---

## 2. The Researcher Guide

Went through several rewrites based on direct feedback from Bri, Charlie, Jaskiran, and Dr. Mussmann (Steve), one of the few faculty who had actually run units successfully.

**Final structure includes:**
- What a unit is, written for someone with zero prior context
- Explicit note that not every unit has a faculty advisor, some may be led by a computational advisor or run without one temporarily
- A designated-representative model: each team sends one person to present, but attendance is not limited to just that person
- A substitute policy if the rep can't attend
- A structured slide template non-attending members fill out before each meeting, including speaker notes so the rep can present accurately
- A concrete deadline: submissions due 5pm the day before the meeting, not vaguely "before"
- Instructions for using an LLM to auto-fill the slide template from a weekly report
- Step-by-step recording instructions (video + attendance + AI summary posted to #time-log)
- A requirement that non-attendees watch the recording and respond to follow-up questions about their own work
- Full enforcement and grading section, tied to real participation grades, not extra credit, which was found not to work at this scale

---

## 3. Automation — Two Slack Bots

Built using Slack Workflow Builder, based on direction from Dima and examples from Kaiyuan's existing bot in another channel.

**Bot 1 — Weekly Report Tracker**
Runs every Friday, asks researchers to confirm they submitted their report and provide a link to it, logs responses to a spreadsheet for staff review.

**Bot 2 — Slide Template Tracker**
Runs before each unit meeting, asks non-attending members to confirm they sent their slide to their rep, logs responses the same way.

Both address the core problem identified in the audit: tracking 100+ researchers manually isn't feasible for a 4-person staff. The bots don't replace human judgment, they surface who needs follow-up.

---

## 4. Unit Formation & Assignment Guide

A separate, shorter doc aimed at admin rather than researchers, written after Bri pointed out that how units get formed and how projects get assigned to them was just as undocumented as the meetings themselves.

**Covers:**
- A lightweight checklist for assigning a project to a unit based on technical method, not application domain
- Named the real edge case Bri raised (a project's focus can shift over time, e.g. Bird Audio moving from image processing to a UI tool) as an open limitation, not something forced into a rigid policy
- Criteria for when a unit should be dissolved, based on what actually happened to r-scripting and 3D vision
- Flagged process ownership as an open question for Bri to resolve

---

## 5. Video Tutorials (PM-Led)

Reassigned Minkyung and Arjun from document editing to building two short video walkthroughs, one for researchers and one for faculty, based on Bri's suggestion that this was a better use of their time and would double as a feedback-gathering tool. Wrote detailed requirements for both videos and reviewed their first researcher-facing script draft, catching a factual error (12 vs. 24-hour deadline) and several missing requirements before it moved to production.

---

## 6. The Manuscript

Once Bri confirmed the guide was solid enough to formalize, shifted focus toward writing this up as a paper rather than just internal documentation.

**Key decision, made with Charlie:** the paper should not be framed as a direct extension of FAIR-CS, the related HAAG paper he co-authored with Bri. Instead, FAIR-CS is cited as prior context, and the paper is written to generalize beyond HAAG and beyond academic research organizations specifically, so it doesn't limit its own audience.

**Current draft includes:**
- Introduction
- Related work (FAIR-CS cited, additional literature pass still needed)
- The Problem, formalized from the audit findings
- The Solution, formalized from the guide as a four-principle framework
- Implementation, condensed from the unit formation guide
- Honest limitations section: no survey/IRB data yet, single-organization case study, group formation still relies on judgment

IRB and survey work were intentionally postponed to next semester, since I'm not continuing into the follow-up course. The goal this semester was to leave a complete enough product that someone else, or a future me as a volunteer, could pick up the evaluation phase.

---

## Open Items Going Into Next Steps

- Confirm publication timeline expectations and target venue with Bri and Charlie
- Incorporate Dr. Mussmann's feedback, including a real structural question about meeting format (his experience suggests two 30-minute in-depth presentations may work better than the current standup-hybrid format)
- Finish the literature review pass for the manuscript's related work section
- Decide on continuation path, volunteer vs. follow-up course, for finishing the survey/IRB phase

---

*HAAG — Unit Meetings & Collaboration Initiative | Summer 2026*
