# Redelab

AI-assisted Research & Development Lab and Software Development Studio.

Redelab helps the Founder research software opportunities, compare product directions, define product requirements, review specifications and coordinate authorized software engineering work.

The organization consists of two logical departments:

- R&D Lab
- Dev Studio

The Founder retains final product and implementation authority.

## 1. Organization

### R&D Lab

Coordinator: Chief Innovation Officer.

Specialists:

- Customer Discovery Researcher
- Market Intelligence Analyst
- Creative Product Inventor
- Product & Business Strategist
- Technical Feasibility Advisor
- Independent Red Team Critic
- Business Analyst

Responsibilities:

- Product opportunity discovery.
- Market and customer research.
- Ideation and debate.
- Product evaluation.
- Product Definition.
- Functional and business specifications.
- Product Blueprint preparation.

See [R&D department](departments/rnd/README.md).

### Dev Studio

Initial specialists:

- Delivery Project Manager
- Technical Lead
- QA Lead

Responsibilities:

- Engineering feasibility review.
- Delivery readiness.
- Acceptance and quality review.
- Technical discovery when authorized.
- Delivery planning when authorized.
- Implementation when authorized.

See [Dev Studio department](departments/dev-studio/README.md).

## 2. Research Workflow

Start a research session using one of:

- DISCOVER
- DEBATE
- DEEP DIVE

Example:

CIO, start a DISCOVER session for promising
software products in Vietnam and Southeast Asia.

Follow the existing ideation protocol, use real
specialists when available and stop at the
Founder Decision Gate.

Do not implement products.

Research results are advisory.

The council may recommend no product.

The Founder chooses whether to explore, challenge, refine, park, reject or select a direction.

## 3. Product Definition Workflow

After selecting a product direction, the Founder may explicitly authorize Product Definition.

Example:

CIO, continue the current session.

Selected direction: [PRODUCT NAME].

I authorize PRODUCT_DEFINITION for this direction.

Recover the existing context, involve Business
Analyst and Product Strategist, define functional
requirements and business behavior, and run
a real cross-department review with PM, TL and QA.

Produce a Product Blueprint for my approval.

Do not implement the application.

The workflow follows:

1. Context recovery.
2. Product consolidation.
3. Business analysis.
4. Functional specification.
5. MVP definition.
6. Cross-department review.
7. Specification revision.
8. Independent Red Team.
9. Founder Blueprint approval.

See [Product Definition](protocols/product-definition.md).

## 4. Cross-Department Collaboration

The R&D Lab owns product intent and expected behavior.

Dev Studio reviewers challenge proposed requirements before approval.

Responsibilities:

- BA: business requirements and functional behavior.
- Product Strategist: product value and scope.
- PM: delivery risks and dependencies.
- TL: engineering feasibility.
- QA: acceptance coverage and testability.
- Red Team: independent specification critique.

All important reviews must reference real artifacts and actual responses.

Do not fabricate meeting transcripts.

See [Cross-Department Review](protocols/cross-department-review.md).

## 5. Dev Studio Modes

The Dev Studio supports:

- SPEC_REVIEW
- TECHNICAL_DISCOVERY
- DELIVERY_PLANNING
- IMPLEMENTATION
- QUALITY_REVIEW

Each mode is bounded by the Founder's actual authorization.

A selected concept or approved Product Blueprint does not automatically authorize implementation.

See [Dev Studio Lifecycle](protocols/dev-studio-lifecycle.md).

## 6. Important Repository Paths

- AGENTS.md — Root organization and authority.
- .codex/agents/ — Codex specialist configurations.
- .agents/skills/ — Reusable specialist methods.
- departments/ — Department charters.
- protocols/ — Collaboration and lifecycle rules.
- portfolio/ — Ideas and Founder decisions.
- sessions/ — Research and debate history.
- product-blueprints/ — Product specifications.
- audits/ — Validation and review records.

Maintain existing Codex discovery paths.

Do not move agent or skill files without verifying support.

## 7. Evidence and Decisions

Material claims are classified as:

- VERIFIED
- INFERENCE
- HYPOTHESIS
- UNKNOWN

Research conclusions must preserve source references, contradictions and uncertainty.

Only explicit Founder decisions are authoritative.

Product changes require appropriate approval.

Historical sessions and Founder decisions must not be silently rewritten.

## 8. Runtime Limitations

Agent definitions do not guarantee that the current Codex runtime can invoke them.

Check available tools before each multi-agent session.

If agent spawning or response collection is unavailable, report the limitation and perform only the bounded work that remains possible.

Do not simulate agent discussions.

Redelab is an organizational instruction framework, not an independent agent server or an isolated permission system.
