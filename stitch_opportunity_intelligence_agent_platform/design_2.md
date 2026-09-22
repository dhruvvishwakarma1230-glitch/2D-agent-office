# Opportunity Intelligence — UI Design Specification

## 1. Design Direction

Build the website as a **clean professional opportunity platform with a distinctive pixel-art agent office**.

The product has two visual layers:

1. **Agent Office:** playful, interactive, pixel-art visualization of the agents working.
2. **Opportunity Workspace:** clean, professional, information-first interface for the actual results.

The pixel-art office is the product's personality and workflow visualization.

The results UI is the product's professional working environment.

### Reference asset

Use `./office-reference.png` as the primary visual reference for the office.

The office should closely reproduce the reference's:

- pixel-art character proportions;
- pixel density;
- warm cream background;
- wooden furniture;
- blue chairs;
- blue monitors;
- green plants;
- dark pixel outlines;
- slightly top-down RPG-office composition;
- manager office at the top;
- eight employee desks below.

Do not replace the visual style with a different pixel-art aesthetic.

---

# 2. Do NOT Make the Entire Website Look Like an AI Demo

This is a critical requirement.

The product should **not** look like:

- an AI presentation;
- a futuristic control center;
- an "agent swarm" visualization;
- a neon cyberpunk dashboard;
- an excessive-gradient SaaS landing page;
- a Slope-style AI canvas;
- a collection of giant floating AI cards.

Avoid making "AI" the visual subject of every screen.

The user is here to find and evaluate opportunities.

The UI should prioritize:

**opportunities → evidence → match → preparation → action**

not:

**agents → animations → effects**

---

# 3. Professional UI Language

For the main website UI, use a professional information-product language similar to established career/networking platforms.

Desired qualities:

- clean;
- trustworthy;
- structured;
- readable;
- compact;
- calm;
- familiar;
- responsive.

Use:

- white/light neutral backgrounds;
- subtle gray borders;
- restrained blue accents;
- dark text;
- compact cards;
- consistent spacing;
- simple buttons;
- clear tabs;
- readable metadata.

Avoid:

- multiple gradients;
- glassmorphism everywhere;
- excessive shadows;
- giant rounded containers;
- oversized headings;
- neon colors;
- excessive animations.

---

# 4. Screen Structure

## Screen A — Search / Agent Office

This is the distinctive entry experience.

The user enters the opportunity request at the top.

Example:

**What opportunity are you looking for?**

`[ Find AI research internships in India...                 ] [Search]`

Below it is the pixel-art office.

The search bar should remain visually clean and readable.

Do not put the search UI into a giant futuristic command center.

---

# 5. Office Layout

Follow the supplied reference image closely.

### Manager office

Top-center:

- glass office;
- manager behind desk;
- monitor;
- small desk plant/accessories;
- shelves;
- wall decorations;
- office door/opening.

### Employee workspace

Below manager:

- 8 desks;
- two rows of four;
- one agent per desk;
- blue chairs;
- monitors;
- small desk accessories.

### Supporting furniture

Use the reference-style:

- bookshelf;
- plants;
- water cooler;
- clock;
- scanner/printer;
- sofa;
- storage furniture.

Keep the office spacious enough for character movement.

---

# 6. Agent Characters

Use eight small pixel-art employees.

They should resemble the supplied reference.

Do not use large illustrated portraits.

Suggested identity:

| Agent | Hair / visual identifier |
|---|---|
| Planner | Black |
| Discovery | Pink |
| Investigator | Blond |
| Verifier | White/silver |
| Match | Brown |
| Application | Dark blue |
| Outreach | Orange/brown |
| Monitor | Purple |

Manager:

- dark hair;
- formal office clothing;
- visually distinct;
- positioned inside manager office.

---

# 7. Search Flow

When the user submits:

`Find AI research internships in India`

the office becomes active.

### State 1 — Planner

Planner starts working.

Above the Planner:

`Analyzing request...`

Then:

`Creating search plan...`

Then:

`✓ Plan ready`

The Planner stands up.

---

# 8. Physical Handoff

The employee must visibly walk to the next agent.

Sequence:

```text
Agent working
     ↓
Task completes
     ↓
Agent stands
     ↓
Agent walks
     ↓
Work handoff
     ↓
Next agent begins
```

Do not replace this with a progress bar.

The physical movement is part of the storytelling.

---

# 9. Comment Bubbles

Each active agent displays a small pixel-art speech/comment bubble.

Bubble characteristics:

- cream/white fill;
- dark pixel border;
- small tail;
- pixel-friendly text;
- compact dimensions.

Examples:

### Planner

`Analyzing request...`

### Discovery

`Searching job listings...`

### Investigator

`Researching organization...`

### Verifier

`Cross-checking deadline...`

### Match

`Comparing your skills...`

### Application

`Preparing application...`

### Outreach

`Finding relevant contacts...`

### Monitor

`Checking opportunity status...`

The bubble should explain the work without becoming a dashboard.

---

# 10. Agent States

Use subtle visual states.

### Idle

- seated;
- normal monitor.

### Working

- subtle monitor activity;
- slight character animation;
- comment bubble.

### Completed

- `✓ Complete` bubble;
- agent stands.

### Handoff

- character walks to destination.

### Waiting

- character remains seated;
- no excessive visual effect.

Avoid glowing outlines, animated rings, neon particles, and giant labels.

---

# 11. Agent Order

Default demo workflow:

```text
Planner
   ↓
Discovery
   ↓
Investigator
   ↓
Verifier
   ↓
Match
   ↓
Application
   ↓
Outreach
   ↓
Monitor
```

Then:

```text
Monitor
   ↓
Manager
```

The real system remains orchestrated and conditional; this sequence provides a clear demo visualization.

---

# 12. Final Report Handoff

After Monitor completes:

1. Monitor stands.
2. Monitor walks to Manager.
3. Monitor gives Manager the report.
4. Manager takes the report.
5. Manager walks to scanner.
6. Manager scans it.

Scanner animation:

- report placed into scanner;
- scanner activates;
- pixel scan line moves across page;
- scan complete.

Then transition to the professional results workspace.

---

# 13. Results Workspace

The results page should be **clean and professional**.

It should not continue the heavy pixel-art aesthetic.

Use a normal web-app interface with subtle references to the office.

### Header

`Opportunity Intelligence`

Search/refine input:

`Find AI research internships in India`

Actions:

- Refine search
- Save search

### Summary row

Example:

`8 opportunities found`

`5 verified`

`2 need attention`

`3 monitored`

Keep this compact.

---

# 14. Opportunity List

Use a familiar professional list layout.

Each opportunity card should contain:

### Main

- opportunity title;
- organization;
- opportunity type;
- location.

### Important metadata

- deadline;
- current status;
- eligibility.

### Match

- matched skills;
- gaps;
- preference fit.

### Evidence

- source;
- verification status;
- last checked.

### Action

- View details;
- Save;
- Prepare application.

Do not make cards huge.

The user should be able to scan many opportunities quickly.

---

# 15. Opportunity Detail Page

Use a clean two-column layout on desktop.

### Main column

#### Overview
Opportunity description and important facts.

#### Requirements
Clear requirement list.

#### Match
Show:

- eligibility;
- skill matches;
- preference fit;
- research alignment;
- skill gaps.

#### Application preparation

- resume suggestions;
- cover letter;
- answers;
- checklist.

#### Outreach

- relevant contacts;
- why the person is relevant;
- drafted outreach.

### Right column

Compact metadata panel:

- deadline;
- location;
- organization;
- current status;
- last verified;
- source.

Primary actions:

`Apply`

`Prepare Application`

`View Source`

`Contact / Outreach`

Actions that send or submit externally must enter an approval step.

---

# 16. Evidence Presentation

Evidence should be highly visible but not visually noisy.

Example:

`Deadline: 12 Oct 2026`

`Verified from official source`

`Last checked: 2 minutes ago`

`View evidence`

When evidence conflicts:

`Uncertainty detected`

`Sources disagree on deadline`

Then expose the supporting sources.

Never hide uncertainty behind an AI-generated certainty label.

---

# 17. Match Presentation

Do not use a single giant "AI Match Score" as the core representation.

Instead expose transparent dimensions:

- Eligibility
- Skill match
- Preference fit
- Research alignment
- Skill gaps
- Uncertainty

This matches the product requirements and keeps the output interpretable.

---

# 18. Approval Gate

Before external actions:

Open a clean confirmation panel.

For email:

```text
To:
Subject:
Message:

Why this contact:
Supporting evidence:

[Cancel] [Approve & Send]
```

For application submission:

```text
Application ready

Documents:
Resume
Cover letter
Answers

[Review] [Approve Submission]
```

The user remains in control of external/irreversible actions.

---

# 19. Activity Timeline

Include an understated timeline showing:

`Search → Evidence → Reasoning → Output → Draft → Approval → Action`

This should be functional and readable, not a flashy animated node graph.

---

# 20. Monitoring

The watchlist should look like a normal professional dashboard.

Each monitored opportunity shows:

- status;
- last checked;
- changed fields;
- alert state.

Example:

`Deadline changed`

`Previously: 12 Oct`

`Now: 19 Oct`

`Re-verification required`

---

# 21. Typography

## Office

Use a pixel-compatible font for:

- agent bubbles;
- tiny labels;
- office signs.

## Professional UI

Use a clean modern sans-serif.

Prioritize:

- readability;
- hierarchy;
- compact metadata;
- accessible contrast.

Do not use pixel fonts throughout the entire website.

---

# 22. Color Strategy

### Office

Use the reference palette:

- cream;
- warm wood;
- pastel blue;
- green plants;
- dark brown outlines;
- restrained character colors.

### Professional UI

Use:

- white;
- neutral grays;
- dark text;
- restrained blue accent;
- semantic status colors only where necessary.

Avoid gradients as a primary visual language.

---

# 23. Motion

Motion should communicate workflow, not decoration.

Required:

- character walking;
- standing/sitting;
- monitor activity;
- speech bubble appearance;
- report handoff;
- manager scanner sequence;
- page transition.

Avoid:

- constant background animation;
- floating particles;
- pulsing gradients;
- excessive hover movement;
- decorative AI effects.

---

# 24. Responsiveness

### Desktop

Primary experience.

Show complete office map.

### Tablet

Scale the office while keeping active agents visible.

### Mobile

Use a controlled office viewport with pan/zoom or focus on the active agent.

The professional results workspace should become a conventional responsive mobile layout.

---

# 25. Key Design Rule

**The office should make the workflow memorable.**

**The results workspace should make the product useful.**

The user should feel:

> "I gave the manager a task. I watched the research team work. Now I have a clean, trustworthy opportunity report."

The visual novelty belongs primarily to the office experience.

The product itself should remain clean, professional, and information-first.
