# Creolytix AI Delivery Model

## 1. Executive Summary
Creolytix uses a governed, AI-assisted delivery model to improve speed, quality, and cross-functional collaboration across product, design, engineering, review, documentation, and release communication.

Because this workflow spans product, design, architecture, engineering, review, documentation, and release communication, the document should also rely on visual explanation wherever helpful. Doodle-style workflow diagrams, annotated screenshots, and simple process illustrations are used throughout this document to make the operating model easier to understand and easier to adopt across teams.

![Executive workflow summary](images/01-executive-workflow-summary.png)

## 2. Objectives of the AI-Assisted Delivery Model
- Convert raw customer input into structured, delivery-ready engineering work.
- Maintain quality, security, and review discipline while increasing throughput.
- Keep humans accountable for decisions and approvals.

A critical objective of this model is standardization at scale. AI-assisted development can create significant inconsistency if every developer uses different prompts, different local agent configurations, and different ad hoc skills. To avoid a “wild west” environment of fragmented coding agents and localized skill chaos, Creolytix uses workspace-specific Codex plugins and repo-local skills to ensure teams operate within shared design patterns, engineering principles, security guardrails, and delivery conventions.

## 3. AI Tooling Components in the Creolytix Model
### 3.1 ChatGPT for requirement clarification
### 3.2 Codex for implementation planning and engineering acceleration
### 3.3 GitHub Copilot for in-editor implementation support
### 3.4 Greptile for review assistance and context-aware PR analysis

### 3.5 Creolytix Codex Plugin
The Creolytix Codex plugin provides an internal control layer that helps standardize how Codex is used across the organization. Rather than allowing every team or developer to independently define how AI should behave, the plugin creates a shared operating model for AI-assisted work. It supports safer interactions, reusable workflows, and guardrails that reduce risk while improving consistency.

A key advantage of the plugin is that it prevents uncontrolled drift in how AI is used across teams. Without workspace-specific controls, organizations can quickly end up with inconsistent prompting styles, variable coding practices, and fragmented local agent behavior. By standardizing the plugin at the workspace level, Creolytix ensures that developers are guided by the same delivery principles, coding expectations, and security constraints.

### 3.6 Repo-Bound Skills
Repo-bound skills are structured capabilities that are intentionally constrained to a repository, domain, workflow, or role. These skills reduce noise, improve output relevance, and help keep AI outputs aligned with architecture, coding standards, naming conventions, review expectations, and security requirements.

Repo-local skills are especially important because they make AI assistance consistent across contributors working in the same codebase. Instead of every developer inventing local prompts, personal workflows, or disconnected coding agents, repo-bound skills ensure that the same repository-level design patterns, guardrails, and engineering principles are applied consistently. This helps prevent localized skill chaos and creates a more reliable, maintainable engineering environment.

## 4. End-to-End Workflow Overview
1. Capture customer goals and constraints.
2. Clarify requirements and acceptance criteria.
3. Transform requirements into epics/stories/issues.
4. Draft UI concepts and refine with human UX review.
5. Split implementation by UI/UX, frontend, backend, and integrations.
6. Execute coding with Copilot/Codex support.
7. Review PRs using Greptile + human reviewers.
8. Update docs and release notes.
9. Publish customer-facing communication.

This section is supported by a high-level visual that shows the full lifecycle from customer requirement capture through planning, design, implementation, pull request review, documentation, release note preparation, and Intercom publication. A doodle-style end-to-end diagram is especially useful here because it helps readers understand how the tools and roles connect across the delivery process.

![End-to-end delivery workflow](images/02-end-to-end-workflow.png)

## 5. Requirement Intake and Clarification
Raw notes are converted into structured requirements with clear scope, assumptions, constraints, and acceptance criteria.

![Requirement to story transformation](images/03-requirement-to-story.png)

## 6. Story and Issue Planning with GitHub
Work is organized into epics and implementation-ready issues, then tracked by status and ownership in GitHub Boards.

![GitHub Boards planning view](images/04-github-boards-planning.png)

## 7. Using Google Stitch to Accelerate UI Design
Stitch is used to quickly move from requirement intent to initial UI concepts before human UX refinement and feasibility alignment.

This section includes screenshots or example captures where appropriate, especially when showing how product requirements are translated into visual UI concepts. Annotated examples help readers understand where AI-generated design acceleration ends and human UX refinement begins.

![Stitch-assisted design flow](images/05-stitch-design-flow.png)

## 8. Issue Segmentation Across Disciplines
A single initiative is segmented into UI/UX, frontend, backend, and integration issues to improve parallel delivery while preserving contract alignment.

## 9. Implementation Model
Developers implement in small, reviewable increments with traceability back to requirements and acceptance criteria.

## 10. Pull Request Standards
PRs include clear summaries, impacted areas, test evidence, risk notes, and rollout considerations.

## 11. Creolytix Codex Plugin, Workspace-Specific Controls, and Safe Coding Guardrails
The Creolytix Codex plugin exists to make AI usage safer, more consistent, and more aligned with enterprise standards. Rather than allowing unrestricted interaction, the plugin can enforce approved workflows, constrain context, and encourage repository-aware generation patterns. This reduces the risk of unsafe or low-quality outputs while improving engineering consistency.

An important part of this model is the use of **workspace-specific Codex plugins**. These ensure that developers operating in the same organizational environment use a shared AI interaction model rather than creating ad hoc local agent setups. This matters because, without standardization, AI-assisted development can quickly become fragmented. Different developers may follow different prompting styles, different implementation patterns, and different assumptions about architecture, security, and review quality.

Repo-bound and repo-local skills extend that control model further. They allow Creolytix to define how AI should assist within a specific codebase, including what patterns to prefer, what constraints to respect, and what quality expectations to follow. As a result, developers working in the same repository are more likely to produce code that reflects common design patterns, common guardrails, and common engineering principles.

This approach helps prevent a “wild west” of coding agents, where each developer operates with different localized skills, inconsistent design habits, and uneven security practices. Instead, Creolytix creates a governed AI delivery environment where AI assistance is standardized, reviewable, and aligned with the organization’s preferred ways of building software. Human review, auditability, and secure operational boundaries remain central to the process.

Workspace-specific Codex plugins and repo-local skills ensure that developers working in the same environment follow common design patterns, guardrails, and engineering principles. This prevents a “wild west” of disconnected coding agents and localized skill chaos, and creates a governed, repeatable model for AI-assisted software delivery.

Because plugin behavior, guardrails, workspace controls, and repo-local skills can be difficult to understand through text alone, this section includes simple architecture visuals.

### 11.3 Why workspace-specific plugins matter
- Standardization across teams
- Reduced prompt drift
- Shared engineering principles
- Safer AI usage patterns

### 11.4 Why repo-local skills matter
- Repository-specific design patterns
- Consistent implementation style
- Lower architectural drift
- Better code review outcomes

### 11.5 Avoiding local agent sprawl
- Risks of ad hoc skills
- Risks of inconsistent coding agents
- Governance benefits of centralized control

![Workspace plugin and repo-local governance](images/06-plugin-skill-governance.png)

## 12. How GitHub Copilot Is Used in Engineering Delivery
Copilot is used as an implementation assistant for boilerplate, refactoring support, test scaffolding, and speed-up of predictable coding tasks. Engineers remain responsible for correctness, architecture decisions, and security-sensitive logic.

Copilot usage is also more effective when combined with workspace-standardized Codex behaviors and repo-local skills. This ensures that implementation support is not purely individual or improvisational, but guided by the same architecture patterns, review expectations, and coding principles used by the wider team.

## 13. Human Review and Approval Responsibilities
Human reviewers approve architecture-impacting decisions, risk acceptance, contract changes, and release readiness.

## 14. How Greptile Is Configured to Review Pull Requests
Greptile is used to evaluate PR changes in context across frontend/backend boundaries, contracts, and related code paths.

This section includes screenshots or annotated examples of pull request review flows where appropriate. Where screenshots are not appropriate, a simple visual shows how Greptile evaluates frontend and backend context, shared contracts, and codebase relationships when reviewing a PR.

![Greptile review context map](images/07-greptile-review-context.png)

## 15. How Codex and Greptile Work Hand in Hand to Refine Pull Requests
The model uses an iterative feedback loop:
1. Developer opens PR.
2. Greptile provides contextual review feedback.
3. Codex helps interpret and implement fixes.
4. Developer updates PR.
5. Human reviewer validates and approves.

A visual feedback loop diagram is included to show the cycle of PR creation, Greptile review, Codex-assisted refinement, human validation, and final approval.

![Codex + Greptile PR refinement loop](images/08-codex-greptile-loop.png)

## 16. Documentation and Knowledge Capture
Requirements, architecture notes, implementation details, and operational impacts are documented alongside code changes.

## 17. Release Notes Generation
Release notes summarize user impact, technical impact, rollout conditions, and any known constraints.

## 18. Publishing Release Notes to Intercom
Annotated screenshots are used to show how release notes move from draft form into customer-facing publication, highlighting only the elements needed to explain the publishing workflow clearly.

![Intercom release publishing flow](images/09-intercom-publishing-flow.png)

## 19. Example Skill Catalog
- Requirement clarification templates
- Story decomposition templates
- PR summary and review response templates
- Security checklist patterns
- Release communication templates

The skill catalog is not treated as an open-ended collection of isolated prompts owned by individual developers. To remain effective at scale, skills are curated, versioned, and governed at the workspace and repository level. This ensures that teams benefit from standardization rather than drifting into disconnected local prompt libraries and inconsistent AI-assisted practices.

## 20. Governance, Security, and Human Oversight
AI can improve speed and quality, but only when used within a governance framework. In this model, AI assists humans rather than replacing them. Requirements, architecture, code, documentation, GitHub issues, GitHub Boards planning, and release communications still go through review and approval by responsible stakeholders. Repository-bounded access, controlled skills, workspace-specific plugins, and internal guardrails help reduce risk.

A major governance principle is the avoidance of unstructured local AI sprawl. If every developer creates their own local skills, agent patterns, and prompting habits without shared controls, the organization risks inconsistency in code quality, design patterns, architecture decisions, and security posture. By standardizing workspace-level Codex plugins and repository-local skills, Creolytix ensures that AI assistance remains aligned with common engineering principles and delivery standards rather than devolving into a fragmented “wild west” model.

## 21. Benefits, Limitations, and Future Improvements
Benefits include faster iteration, better requirement clarity, stronger review quality, and improved cross-functional handoff visibility. Another major benefit is consistency: workspace-specific plugins and repo-local skills help ensure that teams generate work using shared patterns and principles instead of fragmented local AI practices.

Limitations include dependency on tool quality, variable prompt quality, and the need for strong reviewer discipline. Future improvements include better metrics, stronger policy automation, and richer workspace governance controls.

## 22. Appendices
### 22.1 Example prompt templates
### 22.2 Story decomposition format
### 22.3 PR checklist
### 22.4 Review quality checklist
### 22.5 Documentation update checklist
### 22.6 Release note template
### 22.7 Governance checklist

### 22.8 Suggested Visuals and Screenshots for the Document
- End-to-end workflow doodle
- Requirement-to-story transformation diagram
- Stitch-assisted design flow visual
- Workspace plugin and repo-local skill governance diagram
- Greptile + Codex PR refinement loop
- GitHub Boards planning screenshot or mockup
- Release-note generation and Intercom publishing flow

## Visual Communication Standards for This Document
This document should not rely on text alone. Key workflow elements are supported by doodle-style diagrams, annotated screenshots, and simple visual process maps so that product, design, engineering, and leadership stakeholders can quickly understand the operating model.

Visual standards:
- Use doodle-style diagrams for workflows and governance concepts.
- Use screenshots when real tool interfaces improve clarity.
- Use annotations/callouts to focus attention on critical UI elements.
- Avoid cluttered captures; crop and simplify where possible.
- Pair every important workflow with at least one visual.
