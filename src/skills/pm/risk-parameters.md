# Risk Parameters Reference

Default risk thresholds for the PM skill. These guide the risk review in Phase 5.

## Position Limits

| Parameter | Default | Description |
|-----------|---------|-------------|
| Max Single Position | 20% | Maximum allocation to a single ticker |
| Max Portfolio Exposure | 95% | Total invested vs. cash threshold |
| Min Cash Reserve | 5% | Always keep this much uninvested |

## Loss Limits

| Parameter | Default | Description |
|-----------|---------|-------------|
| Max Daily Loss | 3% | Stop trading for the day if hit |
| Max Drawdown | 10% | Trigger full portfolio review |
| Max Single Trade Loss | 5% | Default stop-loss distance |

## Frequency Controls

| Parameter | Default | Description |
|-----------|---------|-------------|
| Max Daily Trades | 5 | More than this signals emotional trading |
| Frequency Alert | 3 trades / 30 min | Rapid trading = impulse alert |
| Cool-down Period | 15 min | Suggested pause after a loss |

## Confidence Thresholds

| Confidence | Action |
|-----------|--------|
| ≥ 85% | Eligible for larger position (up to 15%) |
| 60-84% | Standard position (5-10%), manual confirm required |
| 40-59% | Small position only (≤ 5%), extra scrutiny |
| < 40% | Do NOT trade — thesis too uncertain |

## Risk-Reward Minimums

| Scenario | Min R:R Ratio |
|----------|--------------|
| High confidence (≥ 80%) | 1.5:1 |
| Medium confidence (60-79%) | 2:1 |
| Low confidence (40-59%) | 3:1 |

## Hard Blocks (Cannot Override)

These conditions ALWAYS block execution:

1. **No stop loss** — Every trade must have a defined exit
2. **Invalidated judgment** — Cannot trade on a thesis proven wrong
3. **Position > 25%** — No single bet this large
4. **Daily loss limit hit** — Done for the day
5. **No rationale written** — Must articulate the logic

## Soft Warnings (Require Acknowledgment)

These flag but don't block:

1. Confidence below 60%
2. Trading against daily sentiment/trend
3. Third or more trade of the day
4. Judgment status is "weakened"
5. Correlated positions exceeding 40% combined
6. Trading in the first/last 15 minutes of session
