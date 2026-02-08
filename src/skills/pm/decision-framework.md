# Decision Framework Reference

Complete lifecycle of a judgment and how it becomes a trade.

## Judgment Lifecycle

```
Created → Active → Weakened → Invalidated
                 ↘ Expired
```

### State Definitions

| State | Meaning | Can Trade? |
|-------|---------|-----------|
| **Active** | Logic holds, variables intact | ✅ Yes |
| **Weakened** | Some supporting evidence cracking | ⚠ Yes, with caution (reduce size) |
| **Invalidated** | Falsification condition triggered | ❌ No — exit existing positions |
| **Expired** | Time horizon passed | ❌ No — must create new judgment |

### State Transitions

| From | To | Trigger |
|------|----|---------|
| Active | Weakened | Key variable shifts adversely; partial invalidation |
| Active | Invalidated | Falsification condition fully met |
| Active | Expired | Time horizon exceeded without resolution |
| Weakened | Active | New evidence restores confidence |
| Weakened | Invalidated | Further deterioration confirms thesis is wrong |
| Weakened | Expired | Time horizon exceeded |

## Decision Brief Flow

```
1. User has a JUDGMENT (thesis about a ticker)
         │
2. User wants to ACT → Generate DECISION BRIEF
         │
3. Decision Brief undergoes RISK REVIEW (6 dimensions)
         │
    ┌─────┴─────┐
    │            │
  PASSED      BLOCKED
    │            │
4. APPROVE    Cannot
   (manual     proceed
   confirm)
    │
5. EXECUTE
    │
6. RECORD → goes to daily snapshot → VAULT
```

## Decision Quality Matrix

| Criteria | High Quality | Low Quality |
|----------|-------------|-------------|
| Thesis | Specific, falsifiable | Vague, unfalsifiable |
| Direction | Clear long/short | "It might go up" |
| Confidence | Specific number with reasoning | "Pretty confident" |
| Variables | Listed with measurement criteria | "It feels right" |
| Invalidation | Concrete conditions | None stated |
| Entry | Specific price or range | "Around here" |
| Stop Loss | Defined with logic | None or arbitrary |
| Position Size | Based on confidence & risk | "All in" or random |

## Daily Audit Chain

Every trading day should produce this chain of evidence:

```
Morning Briefing
  └─ Boundary Conditions set
  └─ Judgments checked/created

Intraday Monitoring
  └─ Judgment status updates
  └─ Deviation alerts (if any)
  └─ Opportunity flags (if any)

Decision Briefs (if trades attempted)
  └─ Risk review results
  └─ Approval/rejection

Trade Records
  └─ Entry details
  └─ Exit details (when closed)
  └─ P&L calculation

Post-Market Review
  └─ 4-dimension scoring
  └─ Lessons extracted
  └─ Tomorrow's focus
```

This chain is what transforms random trading into a systematic, reviewable practice.

## Key Questions by Phase

| Phase | The Question |
|-------|-------------|
| Pre-Market | "Under what conditions should I NOT act today?" |
| Judgment | "What would prove me wrong?" |
| Intraday | "Does my morning judgment still hold?" |
| Decision | "Can I articulate this logic in writing?" |
| Risk | "Is what I'm doing now the same thing I said this morning?" |
| Execution | "Have all prerequisites been met?" |
| Review | "Which mistakes were avoidable?" |
