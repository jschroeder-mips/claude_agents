# Claude Code Agent Library

A curated collection of **18 specialized AI agent personas** for [Claude Code](https://code.claude.com/docs/en/sub-agents) subagents. Each agent provides expert-level guidance in specific domains—from technical architecture to business strategy.

## Quick Start

### Installation

Copy agent files to your Claude Code agents directory:

```bash
# For user-level agents (available across all projects)
mkdir -p ~/.claude/agents
cp agents/*.md ~/.claude/agents/

# For project-level agents (available in current project only)
mkdir -p .claude/agents
cp agents/*.md .claude/agents/
```

### Usage

Once installed, Claude Code will automatically invoke agents when appropriate. You can also explicitly request an agent:

```
> Use the technical-lead-archie agent to review my API design
> Have the code-quality-inspector agent check my recent changes
> Ask the github-commit-specialist agent to help commit these changes
```

View and manage installed agents:
```
/agents
```

---

## Agent Catalog

### Technical Agents

| Agent | File | Model | Description |
|-------|------|-------|-------------|
| **A.R.C.H.I.E.** | `technical-lead-archie.md` | sonnet | Technical lead for Cloud (AWS/GCP/Azure), Python, TypeScript, and Godot Engine. Provides architectural decisions, code reviews, and mentoring. |
| **A.P.I.** | `api-design-specialist.md` | haiku | REST and GraphQL API design specialist. Covers resource modeling, versioning strategies, and OpenAPI documentation. |
| **T.E.S.T.** | `test-strategy-architect.md` | haiku | Testing strategy architect for pytest, Jest, Vitest, Playwright, and Godot GUT. Designs test pyramids and fixes flaky tests. |
| **Q.A.I.** | `code-quality-inspector.md` | haiku | Code review specialist analyzing correctness, readability, performance, security, and testability. |
| **D.E.B.U.G.** | `debugging-detective.md` | haiku | Systematic debugging and root cause analysis. Investigates production issues, performance problems, and cryptic errors. |
| **S.E.C.** | `security-auditor.md` | haiku | Security review and vulnerability detection. Identifies OWASP Top 10 issues, injection flaws, and auth weaknesses. |
| **D.E.V.O.P.S.** | `devops-sre-specialist.md` | haiku | DevOps and SRE specialist for CI/CD, Kubernetes, Terraform, and infrastructure reliability. |
| **G.I.T.** | `github-commit-specialist.md` | haiku | Git workflow expert. Creates conventional commits, organizes changes into atomic commits, and maintains repository hygiene. |
| **D.O.C.** | `technical-documentation-specialist.md` | haiku | Technical writing specialist for API docs, architecture overviews, and code documentation. |
| **C.A.T.S.** | `technical-solution-advocate.md` | haiku | Vendor evaluation and build-vs-buy analysis. Assesses TCO, lock-in risks, and technical proposals. |

### Business & Operations Agents

| Agent | File | Model | Description |
|-------|------|-------|-------------|
| **G.E.N.T.** | `project-manager-gent.md` | haiku | Project manager for agile teams. Facilitates stand-ups, sprint planning, and blocker resolution. |
| **C.E.O.** | `ceo-strategist.md` | haiku | Business strategy and executive guidance. Covers market analysis, competitive positioning, and growth strategy. |
| **C.F.O.** | `cfo-financial-strategist.md` | haiku | Financial planning, budgeting, unit economics, and fundraising strategy. |
| **S.A.L.E.S.** | `sales-strategist.md` | haiku | Sales process optimization, pipeline management, and go-to-market strategy. |
| **G.R.O.W.T.H.** | `marketing-growth-specialist.md` | haiku | Marketing strategy, growth tactics, and brand positioning. |
| **C.S.M.** | `customer-success-specialist.md` | haiku | Customer success, retention strategy, and churn prevention. |
| **H.R.** | `hr-people-strategist.md` | haiku | Talent acquisition, organizational design, compensation, and culture development. |
| **I.N.V.** | `inventory-supply-chain-specialist.md` | haiku | Supply chain optimization, inventory management, and logistics strategy. |

---

## Agent Details

### technical-lead-archie.md

**A.R.C.H.I.E.** (Architectural Counsel & Hands-on Implementation Expert)

```yaml
model: sonnet
tools: Read, Edit, Bash, Grep, Glob, Write
```

**Use when you need:**
- Cloud architecture design (AWS, GCP, Azure)
- Python performance optimization (FastAPI, Django)
- TypeScript/React architectural guidance
- Godot Engine game development expertise
- Code review with educational explanations

**Example invocation:**
```
> My Flask API is taking 3 seconds to respond. Use technical-lead-archie to optimize it.
```

---

### api-design-specialist.md

**A.P.I.** (Application Programming Interface Specialist)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- RESTful API resource modeling
- GraphQL schema design
- API versioning strategies
- OpenAPI/Swagger documentation
- REST vs GraphQL trade-off analysis

**Example invocation:**
```
> Use api-design-specialist to design pagination for our user list endpoint.
```

---

### test-strategy-architect.md

**T.E.S.T.** (Test Strategy Architect)

```yaml
model: haiku
tools: Read, Bash, Grep, Glob
```

**Use when you need:**
- Test pyramid design for your project
- Flaky test diagnosis and remediation
- pytest fixture patterns
- Jest/Vitest/Playwright configuration
- Test coverage prioritization

**Example invocation:**
```
> Our E2E tests keep failing in CI. Use test-strategy-architect to fix them.
```

---

### code-quality-inspector.md

**Q.A.I.** (Quality Assurance Inspector)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- Systematic code review before PR submission
- Performance bottleneck identification
- Security vulnerability detection
- Best practices validation (PEP 8, ESLint)
- React/TypeScript anti-pattern detection

**Example invocation:**
```
> Use code-quality-inspector to review my new authentication module.
```

---

### debugging-detective.md

**D.E.B.U.G.** (Debugging Detective)

```yaml
model: haiku
tools: Read, Bash, Grep, Glob
```

**Use when you need:**
- Production bug investigation
- Stack trace analysis
- Performance degradation diagnosis
- Race condition identification
- Memory leak detection

**Example invocation:**
```
> We're getting random 500 errors in production. Use debugging-detective to investigate.
```

---

### security-auditor.md

**S.E.C.** (Security Auditor)

```yaml
model: haiku
tools: Read, Bash, Grep, Glob
```

**Use when you need:**
- OWASP Top 10 vulnerability scanning
- Authentication/authorization review
- Injection flaw detection (SQL, XSS, CSRF)
- Secrets and credential scanning
- Dependency vulnerability assessment

**Example invocation:**
```
> Use security-auditor to review our payment processing code before launch.
```

---

### devops-sre-specialist.md

**D.E.V.O.P.S.** (DevOps & SRE Specialist)

```yaml
model: haiku
tools: Read, Bash, Grep, Glob, Write
```

**Use when you need:**
- CI/CD pipeline design (GitHub Actions, GitLab CI)
- Kubernetes deployment configuration
- Terraform infrastructure as code
- Docker containerization
- Monitoring and alerting setup

**Example invocation:**
```
> Use devops-sre-specialist to set up GitHub Actions for our monorepo.
```

---

### github-commit-specialist.md

**G.I.T.** (Git Specialist)

```yaml
model: haiku
tools: Read, Bash, Grep, Glob
```

**Use when you need:**
- Conventional commit message creation
- Atomic commit organization
- Git history cleanup before merge
- PR description writing
- Changelog generation

**Example invocation:**
```
> I've finished the OAuth feature. Use github-commit-specialist to commit my changes.
```

---

### technical-documentation-specialist.md

**D.O.C.** (Documentation & Organization Conduit)

```yaml
model: haiku
tools: Read, Grep, Glob, Write
```

**Use when you need:**
- API reference documentation
- Architecture decision records (ADRs)
- README and onboarding guides
- Code docstrings and JSDoc
- System design documentation

**Example invocation:**
```
> Use technical-documentation-specialist to document our authentication flow.
```

---

### technical-solution-advocate.md

**C.A.T.S.** (Customer Advocate for Technical Solutions)

```yaml
model: haiku
tools: Read, Grep, Glob, Bash
```

**Use when you need:**
- Build vs buy analysis
- Vendor proposal evaluation
- Total Cost of Ownership (TCO) calculation
- Cloud provider comparison
- Lock-in risk assessment

**Example invocation:**
```
> Should we use Auth0 or build our own auth? Use technical-solution-advocate to analyze.
```

---

### project-manager-gent.md

**G.E.N.T.** (Generative Engagement & Navigation Tool)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- Daily stand-up facilitation
- Sprint planning and retrospectives
- Blocker identification and escalation
- Project status reporting
- Meeting summaries and action items

**Example invocation:**
```
> Use project-manager-gent to prepare our sprint planning session.
```

---

### ceo-strategist.md

**C.E.O.** (Chief Executive Strategist)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- Business strategy development
- Market opportunity analysis
- Competitive positioning
- Organizational prioritization
- Board presentation preparation

**Example invocation:**
```
> Use ceo-strategist to analyze our expansion into the European market.
```

---

### cfo-financial-strategist.md

**C.F.O.** (Chief Financial Strategist)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- Financial modeling and projections
- Unit economics analysis (CAC, LTV)
- Budgeting and resource allocation
- Fundraising strategy
- Cash flow management

**Example invocation:**
```
> Use cfo-financial-strategist to model our runway with different growth scenarios.
```

---

### sales-strategist.md

**S.A.L.E.S.** (Sales Strategist)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- Sales process optimization
- Pipeline management strategy
- MEDDIC/SPIN qualification frameworks
- Pricing strategy
- Go-to-market planning

**Example invocation:**
```
> Use sales-strategist to improve our enterprise sales qualification process.
```

---

### marketing-growth-specialist.md

**G.R.O.W.T.H.** (Marketing & Growth Specialist)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- Growth strategy and experimentation
- Content marketing planning
- SEO and acquisition channels
- Brand positioning
- Campaign performance analysis

**Example invocation:**
```
> Use marketing-growth-specialist to plan our product launch campaign.
```

---

### customer-success-specialist.md

**C.S.M.** (Customer Success Manager)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- Customer health scoring
- Churn prediction and prevention
- Onboarding journey design
- QBR preparation
- Expansion revenue strategy

**Example invocation:**
```
> Use customer-success-specialist to design our customer health score model.
```

---

### hr-people-strategist.md

**H.R.** (Human Resources Strategist)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- Recruiting process optimization
- Compensation framework design
- Organizational structure planning
- Performance review systems
- Culture development

**Example invocation:**
```
> Use hr-people-strategist to design our engineering leveling framework.
```

---

### inventory-supply-chain-specialist.md

**I.N.V.** (Inventory & Network Virtuoso)

```yaml
model: haiku
tools: Read, Grep, Glob
```

**Use when you need:**
- Inventory optimization
- Demand forecasting
- Warehouse/3PL evaluation
- Supply chain cost analysis
- Logistics network design

**Example invocation:**
```
> Use inventory-supply-chain-specialist to optimize our reorder points.
```

---

## Task Tracking Workflow

All agents support a **Task Tracking Workflow** for complex, multi-step tasks. This enables:

- **State persistence** across memory compaction events
- **Progress tracking** for iterative work
- **Parallel agent operation** without file conflicts
- **Recovery** from session interruptions

For complex tasks, agents create three tracking files in the working directory:

| File | Purpose |
|------|---------|
| `{task-id}-context.md` | Goal, constraints, and important context that must persist |
| `{task-id}-todos.md` | Checklist of items to process with progress markers |
| `{task-id}-insights.md` | Findings, recommendations, and results (iteratively updated) |

Use descriptive task identifiers (e.g., `auth-audit`, `api-migration`) to enable multiple agents to work simultaneously without conflicts.

---

## Customization

### Adjusting Tool Access

Edit the YAML frontmatter to restrict or expand tool access:

```yaml
---
name: code-reviewer
tools: Read, Grep, Glob  # Read-only access
---
```

Available tools: `Read`, `Edit`, `Write`, `Bash`, `Grep`, `Glob`, `WebFetch`, `TodoRead`, `TodoWrite`

### Changing Models

Specify model preference in frontmatter:

```yaml
---
model: sonnet   # For complex reasoning tasks
model: haiku    # For fast, simple tasks  
model: opus     # For most capable reasoning
model: inherit  # Use main conversation's model
---
```

### Adding New Agents

1. Create a new `.md` file following the structure pattern
2. Define clear specialization (avoid overlap with existing agents)
3. Include 3+ usage examples in the `description` field
4. Test with `/agents` command

---

## Contributing

This project is licensed under **AGPL-3.0**. Contributions and derivative works must be open-sourced under the same license.

### Quality Checklist

- [ ] YAML frontmatter is valid (`name`, `description`, `model`, `color`)
- [ ] Description includes trigger phrase "Use this agent when..."
- [ ] Agent has clear, non-overlapping specialization
- [ ] Core Principles are domain-specific (not generic)
- [ ] Includes concrete examples from the domain
- [ ] Length is appropriate (~100-300 lines)

---

## License

[AGPL-3.0](LICENSE) - GNU Affero General Public License v3.0

Derivative works must be open-sourced under the same license.
