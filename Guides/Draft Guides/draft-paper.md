# Facilitating Cross-Disciplinary Collaboration in Distributed Research Organizations: A Practitioner Case Study


---

## Abstract

*[To be finalized last. Draft placeholder below.]*

Large, distributed research organizations increasingly rely on cross-disciplinary collaboration to scale their output, yet the coordination structures that support this collaboration are often left informal, inconsistent, or dependent on individual initiative. This paper presents a case study of redesigning the collaboration layer of a large, volunteer-driven research organization. Through a structured audit of communication patterns across multiple teams over two semesters, we identify recurring failure patterns in ad hoc collaboration efforts and propose a lightweight, enforceable framework, built around designated representation, structured knowledge artifacts, and automation-assisted accountability, to address them. We report on our implementation experience, discuss early observations, and outline a plan for formal evaluation. This work offers practical guidance for any organization managing distributed, cross-disciplinary teams at scale.

---

## 1. Introduction

Organizations that bring together contributors from different disciplines or specialties face a persistent challenge: individual teams may collaborate effectively within their own scope, but knowledge, tools, and lessons learned rarely transfer *across* teams without deliberate structure. This is especially true in large, distributed, and often volunteer-driven research organizations, where participants juggle competing time commitments and turnover is frequent.

Cross-team collaboration is valuable for two main reasons. First, it reduces duplicated effort, if one team has already solved a problem, other teams working on related challenges should be able to access that knowledge rather than re-solving it independently. Second, it increases access to specialized expertise, allowing contributors to benefit from advisors or experts outside their immediate team.

Despite this value, cross-team collaboration structures are often the least formalized part of an organization's operations. Individual project or team-level coordination tends to receive more attention and infrastructure, while the layer that connects teams to each other is frequently left to informal norms, inconsistent scheduling, and the goodwill of a small number of highly engaged individuals.

This paper presents a case study of one such organization's effort to redesign its cross-team collaboration structure. We document the failure patterns observed in its prior, informal approach, present a redesigned framework intended to address those patterns, and describe our early implementation experience.

---

## 2. Related Work

Prior work has explored structured mentorship and research operations in large-scale, distributed academic settings, including frameworks for pairing researchers with subject-matter and technical mentors, allocating shared administrative labor across participants, and supporting mentor development over time [CITE: FAIR-CS]. That body of work establishes how individual mentor-mentee and project-level relationships can be structured to scale research operations, and identifies, as an area for future work, the challenge of coordinating a distributed network of researchers beyond their individual project relationships.

This paper addresses that adjacent challenge directly: not the structure of individual mentor-researcher pairings, but the structure of the cross-team collaboration layer that sits alongside them. While informed by and situated within the same broader context as this prior work, the framework presented here is designed to generalize beyond any single organization's structure or terminology, and is intended to be applicable to any group coordinating distributed, cross-disciplinary contributors at scale, academic or otherwise.

*[Additional related work to add: literature on communities of practice, coordination overhead / articulation work in distributed teams, boundary objects, and workspace awareness. To be filled in during a literature pass.]*

---

## 3. The Problem: Why Cross-Team Collaboration Breaks Down

To understand why cross-team collaboration was failing, we conducted a structured audit of communication activity across multiple teams over two semesters, examining both team-level channels and dedicated cross-team collaboration spaces.

### 3.1 Method

We reviewed message history in all cross-team collaboration spaces from the two most recent semesters, along with a targeted sample of individual team channels selected for evidence of sustained, active collaboration. Rather than reviewing every team channel in full, we prioritized identifying channels with clear, ongoing cross-member engagement and examined what specifically differentiated them from inactive channels.

### 3.2 Findings

Several consistent patterns emerged:

**Coordination resets with no continuity.** Every cross-team space we reviewed required a full scheduling reset at the start of each new term, with no carryover of prior scheduling, norms, or cadence from the previous term. This suggests that whatever coordination structure existed was not persisting independently of the specific individuals present at any given time.

**A single point of failure drives most successful collaboration.** In nearly every case where a cross-team space showed sustained activity, that activity traced back to one individual voluntarily taking on informal coordination work, sending reminders, collecting updates, and prompting participation. When that individual's engagement lapsed or ended, so did the space's activity. This is a structurally fragile pattern: the system's function depended entirely on unpaid, uncredited individual initiative rather than any designed mechanism.

**Advisor or leader engagement was the strongest predictor of activity, but for the wrong reason.** Spaces led by an unusually engaged advisor showed meaningfully higher activity than others. However, this reflects the same single-point-of-failure pattern rather than a property of the collaboration structure itself: these spaces were not more effectively designed, they were simply better resourced by one person's discretionary effort.

**Newcomers frequently lacked basic orientation.** Multiple participants, in more than one collaboration space and across more than one semester, asked what the space was for or what was expected of them, in some cases after having already attended a session. This points to an absence of structured onboarding for new participants entering an existing collaboration space.

**Structured artifacts correlated with sustained activity.** Where cross-team spaces did show organic engagement between scheduled sessions, it was consistently associated with the presence of some shared, structured artifact, a task tracker, a recurring automated reminder, or a consistently formatted status update, rather than open-ended discussion prompts.

### 3.3 Implication

Taken together, these findings suggest that cross-team collaboration failures were not primarily about a lack of willingness to collaborate. Rather, they reflect the absence of durable structure: no persistent scheduling mechanism, no distributed responsibility model, no onboarding process, and no default shared artifact for capturing and transferring knowledge across teams. Collaboration was happening, inconsistently, and only where an individual chose to sustain it by hand.

---

## 4. The Solution: A Framework for Structured Cross-Team Collaboration

Based on these findings, we designed a lightweight framework intended to address each identified failure pattern directly, while remaining low-overhead enough to be sustainable in a volunteer-heavy, time-constrained environment.

### 4.1 Design Principles

The framework is built around four principles:

1. **Distribute responsibility rather than concentrate it.** Coordination work should not depend on one highly engaged individual. Responsibilities should be explicitly defined and distributed across all participants, with a single point of contact used only to reduce coordination overhead, not to bear the full workload alone.
2. **Make expectations explicit, not assumed.** Every requirement should be stated with enough specificity that no participant can reasonably claim they did not know what was expected of them.
3. **Use structured, reusable artifacts.** Knowledge transfer between team members and between teams should be captured in a consistent, structured format rather than left to informal verbal relay, which is prone to information loss.
4. **Automate accountability, not judgment.** Lightweight automation should track whether expectations were met, freeing a small administrative staff from manual tracking at scale, while leaving substantive review and judgment to human oversight.

### 4.2 The Representation Model

Rather than requiring every member of a team to attend every cross-team session, each team designates one representative to attend on the team's behalf. This reduces scheduling overhead without limiting participation, any number of team members may attend if they choose, and the representative role can be filled by different people from meeting to meeting.

Team members who are not attending a given session are responsible for providing the representative with a structured summary of their recent work, using a shared template (see Section 4.3). The representative is responsible for representing that work accurately, and if a representative cannot attend, responsibility falls on the team to arrange coverage.

This addresses the single-point-of-failure pattern identified in Section 3.2 by ensuring that the coordination role is a defined, shared team responsibility rather than the informal province of one especially engaged individual.

### 4.3 Structured Knowledge Artifacts

Each non-attending contributor completes a short, structured template before each session, capturing: what they worked on, what it means for the broader project, what they plan to work on next, and any open questions or blockers. This artifact serves two purposes: it gives the representative enough context to present the work accurately to others, and it creates a durable, reviewable record of progress that does not depend on any one person's memory or verbal relay.

We additionally explored the use of large language models to reduce the friction of completing this artifact: contributors can supply their regular progress report to an LLM alongside the template and receive a completed draft in significantly less time than manual completion, which they then review and finalize themselves before submission.

### 4.4 Distributed Onboarding

To address the onboarding gap identified in Section 3.2, the framework requires that foundational information, what the collaboration space is, what is expected of participants, and how to engage with it, be documented explicitly and be the first artifact any new participant encounters, rather than left to be explained informally or inferred from observation.

### 4.5 Lightweight Automation for Accountability

To sustain this structure at scale without placing continuous manual tracking burden on a small administrative staff, we implemented lightweight, scheduled automation that: (1) prompts participants for required submissions at appropriate intervals, (2) logs responses to a shared, reviewable record, and (3) surfaces non-responders for human follow-up rather than escalating automatically. This preserves human judgment in any consequential decision while removing the need for manual reminder and tracking work.

---

## 5. Implementation

We are in the process of piloting this framework within the organization studied in Section 3. Implementation includes:

- Formalized guidance documentation, written to be understandable by a first-time participant with no prior context
- A structured knowledge-artifact template, distributed alongside guidance on optional LLM-assisted completion
- Two lightweight automated accountability workflows, covering recurring progress reporting and pre-session artifact submission
- A companion process document for organizational administrators, describing how cross-team groupings are formed and by what criteria projects are assigned to them, since inconsistent or undocumented grouping decisions were identified as a related, secondary contributor to collaboration failure

We do not yet have outcome data on the framework's effectiveness, discussed further in Section 6.

---

## 6. Limitations and Future Work

This work is presented as an early-stage case study, not a controlled evaluation. Several limitations should be noted.

**No formal outcome data yet.** At the time of writing, the framework has been designed and partially implemented, but has not yet been evaluated through a formal survey or comparative study. A planned follow-up phase includes an IRB-approved survey to assess participant-reported satisfaction, perceived clarity of expectations, and retention, to be conducted in a subsequent term.

**Single-organization case study.** All findings and design decisions are grounded in observation of one organization. While we have intentionally generalized the framework's language and structure to support adoption elsewhere, its effectiveness in other organizational contexts has not yet been tested.

**Group formation remains only partially systematized.** While we propose lightweight criteria for assigning contributors to cross-team groups, this process still relies substantially on administrator judgment, and we identify group-formation quality itself as a possible secondary contributor to collaboration outcomes, deserving of dedicated future study.

**Automation trust and verification.** Our accountability automation currently relies on self-reported confirmation. We discuss, but have not yet implemented, mechanisms for lightweight spot-verification against actual submitted artifacts.

---

## 7. Conclusion

Cross-team collaboration in large, distributed research organizations is frequently under-structured relative to individual project or mentorship-level coordination, leaving it dependent on inconsistent, individually-driven effort. Through a structured audit of communication patterns across multiple teams, we identified recurring failure patterns, coordination that resets with no continuity, reliance on a single engaged individual, absent onboarding, and lack of shared knowledge artifacts, and proposed a lightweight, distributable framework to address them. While formal evaluation remains future work, we believe the framework and the design principles behind it offer practical guidance for any organization seeking to sustain cross-disciplinary collaboration at scale.

---

## Notes for Revision

- [ ] Confirm FAIR-CS citation format and add to references once venue is selected
- [ ] Add additional related-work citations (communities of practice, coordination/articulation work, boundary objects)
- [ ] Fill in abstract last, after full draft is stable
- [ ] Decide whether to name the organization explicitly or keep it generalized/anonymized depending on venue norms
- [ ] Add data/figures once available (e.g., channel activity comparison, participation rates)
- [ ] Confirm with Bri: framing as "inspired by FAIR-CS" rather than an extension, per Charlie's recommendation
- [ ] Venue shortlist to be finalized next week

