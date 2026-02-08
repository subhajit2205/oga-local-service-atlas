### OGA Local Service Atlas Tracker

This repository contains the Local Government Service Atlas Tracker, a geospatial civic platform designed to track, verify, and monitor public infrastructure and service delivery across African local government contexts.

The project prioritizes auditability, data quality, and long-term reuse. It is designed to support urban and rural environments, low-connectivity usage, and multiple data sources including citizens, governments, and NGOs.

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

### Relationship to Tech Programs, Hackathons & Internships

This project may be developed in part through tech programs. If you are contributing through GSoC, please find your [project standard here](https://github.com/OpenGovAfrica/gsoc/blob/main/docs/project-standard.md) & roadmap [here](https://github.com/OpenGovAfrica/gsoc/issues/20)

Contributors are expected to:
- Build reusable, well-documented components
- Respect long-term maintenance needs
- Treat programs as an entry point, not a finish line

The roadmap and contribution guidelines are designed for continuity beyond any single program.

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
