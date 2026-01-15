# Cloud Migration Intake Questionnaire

## About Your Tool

1. **What does your tool do?** (Describe in 2-3 sentences)

2. **What technology is it built with?**
   - [ ] Excel (with formulas only)
   - [ ] Excel (with VBA/macros)
   - [ ] Microsoft Access
   - [ ] Python / R / MATLAB
   - [ ] FORTRAN / C / C++
   - [ ] Other: _______________

3. **How complex would you say it is?**
   - [ ] Simple — A few calculations or lookups
   - [ ] Moderate — Multiple interconnected calculations or worksheets
   - [ ] Complex — Extensive logic, many inputs, or specialized algorithms

4. **Is there existing documentation** (user guides, flowcharts, or technical notes)?

5. **Is the original developer available** to answer questions about how it works?

---

## Data & Inputs

6. **What data does the tool need to run?**
   - [ ] User enters all inputs manually
   - [ ] Reads from files (Excel, CSV, etc.)
   - [ ] Connects to a database or external system
   - [ ] Uses GIS or spatial data
   - [ ] Other: _______________

7. **How large are typical input files or datasets?** (e.g., "a few hundred rows" or "millions of records")

8. **Does the tool use or produce any sensitive or confidential data** (client PII, financial data, proprietary methods)?

---

## Outputs & Results

9. **What does the tool produce?**
   - [ ] Calculated values or summaries
   - [ ] Reports or formatted documents
   - [ ] Charts or visualizations
   - [ ] Exported files (Excel, PDF, CSV, etc.)
   - [ ] Maps or spatial outputs
   - [ ] Other: _______________

10. **How long does a typical run take?** (seconds, minutes, hours?)

---

## Users & Access

11. **How many people need to use this tool?**
    - [ ] 1-5 users
    - [ ] 6-20 users
    - [ ] 20+ users

12. **Do multiple people need to use it at the same time?**
    - [ ] Yes
    - [ ] No

13. **Who are the intended users?**
    - [ ] Internal staff only
    - [ ] Specific client(s)
    - [ ] Multiple clients (each seeing only their own data)
    - [ ] Public access

14. **How often is the tool used?** (daily, weekly, a few times a year, etc.)

---

## Maintenance & Support

15. **How often does the tool need to be updated?** (e.g., new regulations, updated lookup tables, bug fixes)

16. **Who currently maintains or supports the tool?**

17. **What level of support will users need?**
    - [ ] Self-service (users figure it out)
    - [ ] Documentation and training
    - [ ] Ongoing helpdesk support

---

## Business Needs

18. **Why move this to the cloud?** (Check all that apply)
    - [ ] Make it accessible from anywhere
    - [ ] Allow multiple simultaneous users
    - [ ] Improve reliability or reduce errors
    - [ ] Clients are asking for it
    - [ ] Current version is hard to maintain
    - [ ] Other: _______________

19. **Is there a target deadline or project driving the timeline?**

20. **How critical is this tool to your work?**
    - [ ] Nice to have — delays are acceptable
    - [ ] Important — needed for ongoing projects
    - [ ] Critical — significant impact if unavailable

---
---

# Scoring Rubric (Internal Use)

## Base Effort by Technology (Question 2)

| Technology | Base Hours | Notes |
|------------|------------|-------|
| Excel (formulas only) | 40-80 | Usually straightforward translation |
| Excel (with VBA/macros) | 80-160 | VBA logic requires careful re-implementation |
| Microsoft Access | 120-200 | Database + forms + reports + queries to untangle |
| Python / R / MATLAB | 60-120 | Often cleaner to migrate, may just need wrapper |
| FORTRAN / C / C++ | 100-200 | May wrap as-is or require modernization |

## Multipliers

### Complexity (Question 3)
- Simple: ×0.75
- Moderate: ×1.0
- Complex: ×1.5–2.0

### Documentation & Developer Availability (Questions 4-5)
- Good docs AND developer available: ×0.8
- Some docs OR developer available: ×1.0
- No docs AND developer unavailable: ×1.5–2.0

### Data Integration (Question 6)
- Manual entry only: +0 hours
- File uploads (Excel/CSV): +8-16 hours
- Database connections: +24-40 hours
- GIS/spatial data: +40-80 hours
- Multiple integration types: cumulative

### Output Complexity (Question 9)
- Simple values/summaries: +0 hours
- Formatted reports/PDFs: +16-32 hours
- Charts/visualizations: +16-40 hours
- Maps/spatial outputs: +40-80 hours

### Run Time Architecture (Question 10)
- Seconds (synchronous OK): +0 hours
- Minutes (needs async/queuing): +24-40 hours
- Hours (needs job management, progress tracking): +40-80 hours

### Multi-Tenancy & Access (Questions 11-13)
- Single user or small internal team: +0 hours
- Multiple internal users, basic auth: +16-24 hours
- Single client, client-specific branding: +24-40 hours
- Multi-client with data isolation: +60-120 hours
- Public access: +40-60 hours (security hardening)

### Concurrent Usage (Question 12)
- No simultaneous users: +0 hours
- Yes, simultaneous users needed: +16-32 hours (scaling, state management)

---

## Ongoing Costs (Annual Estimate Factors)

### Hosting (Base)
- Light usage (<100 runs/month): $50-150/month
- Moderate usage (100-1000 runs/month): $150-400/month
- Heavy usage or long-running jobs: $400-1000+/month

### Maintenance & Support (Questions 15-17)
- Stable tool, self-service users: 20-40 hours/year
- Occasional updates, documentation support: 40-80 hours/year
- Frequent updates, helpdesk support: 80-160+ hours/year

### Criticality Adjustment (Question 20)
- Nice to have: Standard SLA
- Important: Add monitoring, +$50-100/month
- Critical: Add redundancy, enhanced monitoring, +$150-300/month

---

## Quick Estimate Formula

```
Total Hours = (Base Hours × Complexity × Documentation Factor)
            + Data Integration
            + Output Complexity  
            + Architecture Adders
            + Multi-Tenancy Adders
```

**Example:** Excel with VBA (base 120) + Moderate (×1.0) + No docs, no dev (×1.75) + Database connection (+32) + PDF reports (+24) + Runs in minutes (+32) + Multi-client (+80) = **378 hours**

---

## Red Flags (Add Contingency or Scope Discussion)

- "I'm not sure how it works" — Add 25-50% contingency
- "It's been modified by several people over the years" — Add 25% contingency
- "It has to match the existing outputs exactly" — Add 20% for validation/QA
- "We need it by [aggressive date]" — Discuss phased approach
- Legacy compiled code with no source — May require full rewrite; scope separately
