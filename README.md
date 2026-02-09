### OGA Local Service Atlas Tracker

This repository is part of the OpenGov Africa (OGA) ecosystem and contains the Local Government Service Atlas Tracker, a geospatial civic platform designed to track, verify, and monitor public infrastructure and service delivery across African local government contexts. It prioritizes auditability, data quality, and long-term reuse. It is designed to support urban and rural environments, low-connectivity usage, and multiple data sources including citizens, governments, and NGOs. 

The project is built with a focus on long-term sustainability, public collaboration, and clear accountability. All development follows OGA-wide project standards to ensure the work remains maintainable, auditable, and reusable beyond any single contributor or cohort.

This repository is intentionally scaffold-first. Early contributors will be laying the foundations & no prior environment or infrastructure is assumed.

---

### Project Goals

- Create a normalized, geospatial registry of public infrastructure assets
- Enable citizen and institutional reporting with strong evidence and provenance
- Support verification, moderation, and discrepancy detection workflows
- Make service delivery failures visible, queryable, and actionable
- Produce reusable civic data suitable for research, advocacy, and governance

### Technical Overview

The platform is built around a geospatial-first, auditable data model with strong provenance guarantees.

Core technical principles:
- All spatial data uses GeoJSON and PostGIS
- GeoJSON as the standard interchange format for all spatial data
- All records are attributable to a source and time
- State changes are explicit, validated, and auditable
- Citizen-submitted data is verifiable, not assumed true
- Official and community data can coexist and be compared
- Normalized geographic areas (no free-text locations)
- Strong provenance and audit trails for all reports and verification actions
- Clear separation between data ingestion, validation, and presentation layers

High-level components:
- PostgreSQL + PostGIS for spatial storage (Geospatial database)
- Backend API enforcing validation for assets, reports, evidence, verification, and workflow rules
- Ingestion pipelines for official infrastructure datasets
- Web-based: Mobile-first web interface for citizen reporting and map interfaces
- Moderation and verification tooling
- Public and admin-facing APIs: Public read-only APIs for maps and analytics
- Analytics and discrepancy detection services

No specific framework is mandated at the start, but contributors must justify and document architectural decisions against the project standards:
- Data durability and portability
- Ease of contribution
- Long-term maintainability
- African deployment realities

---

### Repository Setup (Initial)

This repository begins without a predefined runtime environment.

Expected initial contents:
- Clear documentation before complex code
- Incremental setup scripts, not monolithic installers
- Configuration via environment variables
- Reproducible local development instructions once tooling is introduced

Early commits should prioritize:
- Data models and schema definitions
- API contracts and validation rules
- Documentation of decisions

---

### How We Work: Ownership and Collaboration

This project follows an **individual-ownership, collaborative-development** model across all phases of work, from Phase 0 through final delivery.

Contributors are encouraged to collaborate openly through discussions, peer reviews, and shared problem-solving. However, all implementation work must have clearly attributable ownership. Each task, feature, or deliverable is owned by a single contributor, even when informed by collective discussion or feedback.

Collaboration should strengthen implementation quality, not dilute accountability.

---

### Task Ownership and Coordination

All work coordination and ownership is managed publicly using GitHub Issues and Discussions.

- **GitHub Issues** are the source of truth for task ownership and execution.
- **GitHub Discussions** are used for coordination, planning, and architectural alignment, but do not imply ownership.

Before starting work, contributors should explicitly claim an Issue by commenting on it. Each Issue must have one primary owner. Pull Requests must reference the Issue they close.

The standard workflow is:

Discussion (optional) → Issue (owned) → Pull Request (authored) → Merge → README attribution

---

### Phase-Based Work Structure

Work in this project is organized by phases (e.g. Phase 0, Phase 1, Phase 2).

Each phase typically includes:
- A phase overview Issue
- Individual Issues for each deliverable within that phase
- One primary owner per deliverable

Phase-level credit alone is insufficient; ownership must always map to concrete deliverables.

---

### Phase Review Groups (Peer Review Model)

For each phase, contributors may form a small **Phase Review Group** (typically 2–4 people).

The purpose of the review group is to:
- Review each other’s Pull Requests
- Provide architectural and code-quality feedback
- Share context and reduce knowledge silos

Review groups do **not** imply shared ownership.

Rules:
- Every Pull Request should receive at least one peer review from the Phase Review Group before maintainer approval.
- Reviewers must not push commits directly to another contributor’s branch.
- All implementation changes must be authored and committed by the Pull Request owner.

---

### Pull Request and Review Rules

- Every Pull Request must be linked to a GitHub Issue with a clearly identified owner.
- The Pull Request author is the sole owner of the implementation.
- Reviewers may suggest changes using comments or GitHub’s suggested changes feature, but the author must apply them.
- Peer reviews are encouraged at all stages and are considered a core contribution to the project.

---

### Contributors & Roles

This project follows an individual-ownership, collaborative-development model across all phases of work and maintains explicit attribution for all contributors. Contributors are encouraged to collaborate through discussion, reviews, and coordination at every stage of the project. However, all implemented work must have clearly attributable ownership.

Each contributor is credited with the specific components, tasks, or deliverables they owned or led. Participation, discussion, or review alone does not imply ownership.

| Contributor | Role / Focus Area | Owned Deliverables |
|------------|------------------|--------------------|
| Name / GitHub | Backend, Frontend, Data, Infra, Research | Clearly scoped features, services, or setup tasks |

This table must be kept up to date as the project evolves, from Phase 0 through final delivery. Phase-level credit is insufficient on its own; ownership must always be traceable to concrete deliverables, from initial scaffolding (Phase 0) through final handover.

**Clarification on Collaboration and Ownership (All Phases)**

From Phase 0 through the final phase, contributors may not jointly claim the same implementation output unless responsibilities are explicitly separated and documented. Collaboration should strengthen implementation quality, not dilute accountability.

---

### Definition of Done

A task or feature is considered complete only when all of the following are satisfied:

1. Code is clean, readable, and compliant with project linting and formatting rules.
2. Appropriate unit and/or integration tests are included and CI passes.
3. Relevant documentation is updated (README, ARCHITECTURE, API docs where applicable).
4. Database migrations are provided and reviewed if schema changes are involved.
5. The Pull Request has received at least one peer review and maintainer approval.

---

### Relationship to Tech Programs, Hackathons & Internships

This project may be developed in part through tech programs. If you are contributing through GSoC, MLH, Outreachy etc, please find your [project standard here](https://github.com/OpenGovAfrica/gsoc/blob/main/docs/project-standard.md) & roadmap [here](https://github.com/OpenGovAfrica/gsoc/issues/20). 
_If this becomes obselete please raise an issue for_

Contributors are expected to:
- Build reusable, well-documented components
- Respect long-term maintenance needs
- Treat programs as an entry point, not a finish line

The roadmap and contribution guidelines are designed for continuity beyond any single program.

### GSoC Compatibility Note

GSoC compatibility: Contributors may collaborate through discussion and peer review, but all submitted work must have clear individual ownership and be attributable to a single contributor for evaluation.

---

### Maintainer Enforcement Guidelines

These guidelines apply from Phase 0 through final project delivery.

Maintainers are responsible for ensuring clear ownership and accountability throughout the project lifecycle. When reviewing work, maintainers should verify that:

1. Every pull request has a clearly identifiable primary owner.
2. Each deliverable, regardless of phase, is attributable to a specific contributor.
3. The README “Contributors & Roles” section reflects actual implementation ownership, not participation alone.
4. Multiple contributors are not credited for the same deliverable unless roles and responsibilities are explicitly differentiated.
5. Collaboration is demonstrated through reviews, discussions, and coordination — not shared ownership of identical outputs.

If ownership is unclear at any stage, maintainers should request clarification or restructuring before merging.
Clear ownership is required for all phases to ensure sustainability, accountability, and long-term project health.

---

### Roadmap and Sustainability

#### Foundation Phase
- Contribution workflow established
- Issue labeling and onboarding material (README.md, roadmap.md etc) prepared
- Repository scaffolding: Define canonical data models for geographic areas, infrastructure assets, reports, and evidence
- Establish PostGIS setup with GeoJSON validation
- Document architectural and data model decisions
- Data models defined and reviewed
- Set up basic CI and testing standards

#### Core Platform Phase
- Implement reporting and verification workflows
- Build ingestion pipelines for official datasets
- Expose public and admin APIs
- Geospatial database with PostGIS
- Infrastructure and geographic area models
- Enforce auditability and state transitions
- Basic moderation workflow

#### Public Interface Phase
- Citizen submission tools (mobile-first, low-connectivity aware)
- Interactive map interface
- Public read-only analytics endpoints

#### Analysis and Accountability Phase
- Discrepancy detection between official and citizen data
- Verification and audit trails
- Duplicate and abuse detection
- Temporal logic for stale and recurring issues
- Analytics dashboards and geographic summaries
- Subscriptions and alerts

#### Sustainability Phase
- Public and admin APIs fully documented
- Automated testing and CI enforcement
- Improved documentation and onboarding
- Community governance and review processes (Demo deployment with urban and rural examples)
- Data export and interoperability
- Expanded geographic coverage
- Clear handover documentation

---

### Contribution Guidelines

This project welcomes contributors of all experience levels.

Before contributing, please read:
- The documentation in the `docs/` directory
- [Project Standard](https://github.com/OpenGovAfrica/gsoc/blob/main/docs/project-standard.md)

General expectations:
- Small, reviewable pull requests
- Clear commit messages. (Data model changes require written justification)
- Documentation alongside code. Every feature must be documented.
- All spatial data must use GeoJSON
- No inferred or fabricated data
- All changes & code must be testable and reviewable

Required before submitting a pull request:
- Tests for new logic
- Updated documentation if behavior changes
- Clear explanation of trade-offs

**Code that compromises data integrity, provenance, or auditability will not be accepted.** 

---

### Issue Labels and Onboarding

Issues in this repository are labeled to support contributors of different experience levels.

Common labels:
- good first issue: Safe entry points with limited scope
- beginner: Requires basic familiarity with the stack
- intermediate: Requires understanding of project architecture
- advanced: Complex logic or cross-cutting concerns
- data-model: Schema and validation work
- geospatial: PostGIS, GeoJSON, and spatial queries
- frontend: UI and user experience
- backend: API and business logic
- documentation: Writing or improving docs

New contributors are encouraged to:
1. Read the roadmap and data models
2. Start with a labeled onboarding issue
3. Ask clarifying questions early

---

### Getting Started (Early Contributors)

There is no pre-existing development environment yet.

Early contributions may include:
- Database schema proposals
- Architecture diagrams
- API contract drafts
- Validation rules
- Documentation improvements
- Issue triage and labeling

Do not assume tools or frameworks. Propose them.

---

### Governance and Review

All significant changes require review.

Decisions affecting:
- Data models
- Geographic normalization
- Verification logic
- Public APIs

must be documented in `docs/` and linked from the relevant pull request.

**This project prioritizes institutional memory. If it is not written down, it does not exist.** The goal is a platform that communities, journalists, and governments can rely on to understand the real state of public service delivery.

---

### License and Reuse

This project is intended for open civic use. Licensing details will be finalized early in Phase 0 to ensure maximum reuse and interoperability.
