# Opportunity Intelligence — Product Requirements Document (PRD)

## 1. Product Overview

**Product:** Opportunity Intelligence Agent

Opportunity Intelligence is a stateful multi-agent system that turns opportunity discovery into a closed-loop workflow:

**Discover → Investigate → Verify → Match → Prepare → User Approval → Act → Monitor**

The system is intended for users searching for jobs, internships, research positions, scholarships, hackathons, and related opportunities.

The product should not behave like a simple search engine. Search is only the discovery layer. The system coordinates research, evidence verification, personalized matching, preparation, approval-gated actions, and monitoring.

---

# 2. Problem

Opportunity information is fragmented across jobs, university/lab, company, research, and other web sources.

Users currently have to manually:

- find opportunities;
- verify deadlines, eligibility, and status;
- compare requirements with their own profile;
- identify skill gaps;
- research organizations and relevant people;
- prepare application materials;
- remember follow-ups;
- re-check opportunities because information can change.

A saved opportunity link can become stale.

Search engines provide information, but the user still has to coordinate the workflow themselves.

---

# 3. Product Thesis

Opportunity Intelligence should function as a coordinated research team.

The user gives the system a goal.

The system:

1. understands the goal;
2. creates a research plan;
3. discovers opportunities;
4. investigates promising opportunities;
5. verifies important facts;
6. compares opportunities with the user's profile;
7. prepares application/outreach material;
8. asks for human approval before external actions;
9. monitors selected opportunities for changes.

The product should preserve evidence for important claims and should never invent user qualifications or submit false information.

---

# 4. Primary Users

### Students

Examples:

- internships;
- research opportunities;
- scholarships;
- hackathons.

Value:

Relevant opportunities plus preparation.

### Job Seekers

Examples:

- jobs;
- networking opportunities.

Value:

Fit analysis plus application workflow.

### Researchers

Examples:

- labs;
- research positions;
- collaborators.

Value:

Research alignment plus outreach preparation.

---

# 5. Core User Experience

The product has two major UI modes.

## Mode A — Agent Office

The user enters a request and watches the multi-agent workflow execute inside a pixel-art office.

Example:

> Find AI research internships in India that match my profile.

The office visually represents the agents working.

This visualization is a product interaction layer, not the final report itself.

## Mode B — Opportunity Results

After the workflow finishes, the user receives a professional opportunity-results interface containing the findings, evidence, matching information, preparation material, and relevant actions.

The results interface must be clean, professional, information-dense, and easy to scan.

It should resemble the usability principles of products such as LinkedIn: clear hierarchy, restrained visual decoration, strong typography, structured cards/lists, obvious actions, and high information clarity.

It should **not** look like a flashy AI dashboard, presentation deck, or overly animated "AI agent" showcase.

---

# 6. Search Entry

The primary action on the initial screen is a search bar.

Example:

**What opportunity are you looking for?**

Input:

`Find AI research internships in India`

The user can submit using:

- Enter;
- Search button.

The user's request becomes the workflow goal.

---

# 7. Agent Architecture

The system contains eight specialized agents plus an Orchestrator.

## 7.1 Planner Agent

### Responsibility

Parses the user's goal, constraints, and desired opportunity type.

Creates the research plan.

### Agentic decision

What must be searched and which constraints matter?

### Example

For:

> Find AI research internships in India

the Planner may create a plan involving Jobs + Scholar + Search.

---

## 7.2 Discovery Agent

### Responsibility

Finds candidate opportunities using live search data.

Normalizes results and removes duplicates/noise.

### Agentic decision

Should the query be refined or another search vertical used?

### Example

Searches internship listings, company pages, and research positions.

---

## 7.3 Investigator Agent

### Responsibility

Performs deeper second-hop research on promising opportunities, organizations, labs, recruiters, researchers, and other relevant context.

### Agentic decision

What missing context must be collected before an opportunity can be evaluated?

### Example

After finding a lab internship, researches the lab's research areas and recent work.

---

## 7.4 Verifier Agent

### Responsibility

Cross-checks critical facts such as:

- deadline;
- eligibility;
- active status;
- requirements.

### Agentic decision

Is the evidence strong enough, or should another search be performed?

Conflicting evidence must produce an uncertainty state rather than a fabricated answer.

---

## 7.5 Match Agent

### Responsibility

Compares opportunity requirements with:

- education;
- skills;
- experience;
- preferences.

Identifies matches, gaps, and uncertainties.

### Example

If an opportunity requires CUDA and the profile does not contain CUDA, identify CUDA as a skill gap.

---

## 7.6 Application Agent

### Responsibility

Creates opportunity-specific preparation material including:

- resume emphasis;
- cover letter;
- answers;
- document checklist.

The agent may recommend which genuine parts of the user's profile should be highlighted.

It must never fabricate qualifications.

---

## 7.7 Outreach Agent

### Responsibility

Finds relevant public professional contacts and drafts targeted outreach.

The agent researches why the person is relevant and uses evidence to personalize the draft.

Cold outreach must not be mass-generated or based on fabricated relationships.

---

## 7.8 Monitor Agent

### Responsibility

Periodically re-checks selected opportunities.

Compares the current state with the saved baseline.

Detects meaningful changes and triggers:

- verification;
- replanning;
- user notification.

Example:

If a deadline changes, the opportunity is re-verified.

---

# 8. Orchestrator

The Orchestrator is the control plane, not a separate research agent.

Responsibilities:

- maintain task state;
- route work between agents;
- prevent duplicate work;
- invoke tools;
- handle retries;
- move opportunities through the lifecycle;
- pause at human-approval checkpoints.

Agents do not always run blindly.

The workflow is conditional.

Examples:

- weak discovery → refine search;
- missing evidence → investigate;
- conflicting facts → verify again;
- meaningful monitored change → re-plan.

---

# 9. End-to-End Workflow

1. User provides a goal plus resume/profile and preferences.
2. Planner creates search constraints and delegates discovery.
3. Discovery uses SerpApi to find opportunities and remove duplicates/noisy results.
4. Investigator performs second-hop research when additional evidence is needed.
5. Verifier cross-checks critical fields and marks uncertainty where evidence conflicts.
6. Match produces transparent dimensions such as eligibility, skill match, preference fit, and research alignment.
7. Application prepares opportunity-specific materials.
8. Outreach prepares targeted networking communication when relevant.
9. User reviews and approves any external action.
10. Only after approval can execution send or submit an external action.
11. Monitor watches selected opportunities.
12. A meaningful change triggers verification and re-planning.

---

# 10. Agent Office Demo Interaction

The office screen is an interactive visual representation of the workflow.

## 10.1 Initial State

- Manager is inside the manager office.
- Eight agents are seated at their desks.
- All agents are idle.
- Search bar is available.
- No active-agent bubble is shown.

## 10.2 Active Agent

When an agent receives work:

- their monitor becomes active;
- the character performs a subtle working/typing animation;
- a small pixel-art comment bubble appears above the character;
- the bubble explains the current action.

Example:

`Analyzing request...`

`Creating search plan...`

## 10.3 Completion

When the agent finishes:

- bubble changes to `✓ Complete`;
- agent stands up;
- agent walks to the next agent;
- work is handed off;
- the next agent starts.

The physical handoff is a visual representation of orchestration.

## 10.4 Final Handoff

When the last agent finishes:

1. the final agent stands;
2. walks to the manager;
3. hands over the final report;
4. manager receives the report;
5. manager walks to the scanner;
6. manager places the report in the scanner;
7. scanner animation completes;
8. the results page opens.

---

# 11. Results Page Requirements

The results page is the primary functional output.

It should provide:

- original search goal;
- number of opportunities found;
- opportunity title;
- organization;
- URL;
- deadline;
- requirements;
- eligibility;
- current status;
- evidence;
- baseline where relevant;
- matched skills;
- skill gaps;
- uncertainty;
- application preparation;
- outreach preparation;
- relevant contacts;
- monitoring state.

Important source evidence must remain accessible.

Every material claim should retain its supporting source/search evidence.

---

# 12. Information Architecture

Recommended result-page structure:

### Header

- Opportunity Intelligence
- Current search goal
- Search / refine action

### Summary

- Opportunities found
- Verified opportunities
- Opportunities requiring attention
- Monitored opportunities

### Opportunity list

Each item should expose:

- title;
- organization;
- type;
- deadline;
- location;
- status;
- match information;
- key requirements;
- evidence.

### Opportunity detail

Selecting an opportunity opens:

1. Overview
2. Eligibility
3. Requirements
4. Match
5. Skill gaps
6. Evidence
7. Application preparation
8. Outreach
9. Monitoring

---

# 13. Evidence & Trust

The product must distinguish between:

- explicit listing requirements;
- AI inference;
- user-provided profile facts.

Important claims should have source evidence.

Conflicting evidence should create an uncertainty state.

The system should maintain an activity timeline:

**Search → Evidence → Reasoning → Output → Draft → Approval → Action**

---

# 14. Human Approval Guardrail

The system is autonomous for research and drafting.

External or irreversible actions remain human-approved.

Examples requiring approval:

- sending an email;
- submitting an application;
- other external actions.

The system must:

- show the final action payload;
- identify the recipient/destination;
- allow user review;
- execute only after explicit approval.

---

# 15. Cold Mailing / Outreach

The Outreach Agent should:

1. identify a relevant opportunity;
2. identify a potentially relevant recruiter, professor, researcher, founder, or professional;
3. verify why the contact is relevant;
4. collect personalization context;
5. draft a concise targeted email;
6. show the user the recipient, subject, body, and supporting context;
7. wait for approval;
8. send through an authorized Gmail account only after approval;
9. store outreach status;
10. prepare a follow-up when appropriate.

The product must not:

- mass-email;
- spam contacts;
- fabricate relationships;
- invent qualifications.

---

# 16. Data Model

### Users

- profile;
- education;
- skills;
- preferences;
- documents;
- consent.

### Opportunities

- title;
- organization;
- URL;
- deadline;
- requirements;
- evidence;
- baseline.

### Matches

- eligibility;
- skill matches;
- gaps;
- rationale;
- uncertainty.

### Applications

- status;
- documents;
- approvals;
- actions;
- timestamps.

### Contacts

- public professional identity;
- relevance evidence;
- outreach state.

### Monitoring

- baseline snapshot;
- last check;
- changes;
- alert state.

---

# 17. Technology Stack

### Frontend

React + Vite + Tailwind CSS

Responsibilities:

- web UI;
- agent office;
- agent timeline;
- opportunity dashboard/detail.

### API

Node.js + Express

Responsibilities:

- authentication;
- REST endpoints;
- business logic.

### Agent Runtime

Python + LangGraph

Responsibilities:

- stateful orchestration;
- agent workflows.

### LLM

Gemini API or equivalent

Responsibilities:

- planning;
- extraction;
- matching;
- drafting.

### Database

MongoDB Atlas

Stores:

- profiles;
- opportunities;
- evidence;
- applications;
- monitoring state.

### Search

SerpApi

Search verticals include:

- Google Search;
- Google Jobs;
- Google Scholar;
- Google News;
- Google Maps.

Optional:

- Google Flights;
- Google Hotels.

### Email

Gmail API

### Scheduler

Cron / managed scheduler

### Deployment

Vercel + Render / Cloud Run

---

# 18. MVP Scope

The MVP should prioritize:

- profile/resume ingestion;
- agentic SerpApi discovery;
- Investigator + Verifier loop;
- transparent Match view;
- Application Agent;
- Outreach Agent;
- approval gate;
- Monitor Agent;
- agent office visualization;
- professional opportunity-results page.

The architecture may contain eight agents, but implementation should focus deeply on Discovery + Investigator + Verifier + Match + Action + Monitor, with Planner and Orchestrator coordinating the loop.

---

# 19. Hackathon Demo Narrative

Demo input:

> Find AI research internships in India and help me apply.

Demonstration:

1. User enters request.
2. Planner analyzes request.
3. Discovery searches opportunities.
4. Investigator researches missing lab/organization context.
5. Verifier confirms important facts.
6. Match identifies skill gaps.
7. Application prepares materials.
8. Outreach identifies relevant contacts and prepares a message.
9. User reviews an approval gate.
10. Monitor later detects a controlled change and re-verifies it.

The office animation visualizes these steps.

---

# 20. Success Metrics

### Search relevance

At least 5 useful results from one user goal.

### Evidence coverage

Major claims have supporting source evidence.

### Agentic loop

At least one adaptive or second-hop search is demonstrated.

### Action readiness

One complete application package is generated.

### Monitoring

One controlled change is detected and re-verified.

### Human control

No external action occurs without explicit approval.

---

# 21. Design Principles

## Professional core

The product's core UI should feel like a professional opportunity platform.

Use:

- clean white/light surfaces;
- restrained blue/neutral accent colors;
- strong typography hierarchy;
- compact information cards;
- clear labels;
- familiar list/table patterns;
- obvious primary actions;
- consistent spacing.

## Pixel office as interaction layer

The pixel-art office should provide personality and explain agent activity, but it must not make the complete product look like a game.

## Avoid "AI theater"

Do not use:

- excessive glowing gradients;
- giant "AI" labels;
- unnecessary animated blobs;
- constant particle effects;
- futuristic neon dashboards;
- oversized agent-status cards;
- decorative visual noise;
- presentation-slide layouts.

The interface should communicate useful information before visual spectacle.

---

# 22. Product Success Definition

The user should understand the product in one sentence:

> "I give the system an opportunity goal, its agents research and verify it, compare it with my profile, prepare what I need, and keep watching it for changes."

The system should feel like a **professional opportunity research platform with a distinctive agent-office visualization**, not an AI animation demo.
