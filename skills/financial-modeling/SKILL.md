---
name: financial-modeling
description: "Financial Modeling playbook. Operate like an FP&A analyst who ties every model out to zero before presenting it. Use when the agent is asked to handle formula-first, tie-out checks, revenue base, forecast method, working capital, credit triangle work, or when a teammate @mentions it for anything in the Financial Modeling lane."
---

# Financial Modeling

Operate like an FP&A analyst who ties every model out to zero before presenting it.
FORMULA-FIRST: Every calculated cell is a live formula, never a hardcoded number - only historical actuals and assumption drivers get hardcoded (and flagged, e.g. blue font). One input should cascade through the income statement, balance sheet, and cash flow automatically. A dead hardcoded number is the single most common model defect.
TIE-OUT CHECKS: Four checks must always equal zero - Assets minus Liabilities minus Equity; CF ending cash minus BS cash; IS net income minus CF starting net income; prior retained earnings plus net income plus SBC minus dividends minus ending retained earnings. Any nonzero check means the model is broken, full stop, before anything else gets reviewed.
REVENUE BASE: Compute every margin off NET revenue (gross revenue minus returns, allowances, and discounts), never off gross revenue - using gross systematically overstates the top line and every downstream margin built on it.
FORECAST METHOD: Drive COGS, S&M, G&A, R&D, and SBC as a percentage-of-net-revenue assumption in the projection period, never as hardcoded dollar figures - keep the identical formula structure across every projection column so a driver change flows cleanly.
WORKING CAPITAL: DSO = AR/Revenue x 365, DIO = Inventory/COGS x 365, DPO = AP/COGS x 365; Net Working Capital = AR + Inventory - AP. A rise in AR or inventory is a USE of cash (negative to CFO); a rise in AP is a SOURCE of cash (positive to CFO) - get the sign wrong and the whole cash flow statement breaks.
CREDIT TRIANGLE: Net Debt/EBITDA = (Total Debt - Cash)/LTM EBITDA for leverage, Interest Coverage = EBITDA/Interest Expense for coverage, Quick Ratio = (Current Assets - Inventory)/Current Liabilities for liquidity - track all three together, not leverage alone.
NOL RULES (post-2017 US): Net operating loss utilization is capped at 80% of taxable income; a new entity starts with beginning NOL = 0 and NOL only grows when EBT is negative; taxes are MAX(0, taxable income x rate) - a loss year never produces a negative tax charge, it builds a deferred tax asset instead (DTA = ending NOL x tax rate).
CIRCULARITY: Interest expense feeds net income, which feeds cash, which feeds the debt balance, which feeds interest expense next period - a deliberate circular loop. Enable iterative calculation (cap iterations, cap max change) with a circuit-breaker toggle, or sidestep it entirely by basing interest on the BEGINNING debt balance.
SCENARIO SANITY CHECK: Toggle Base/Upside/Downside and verify the hierarchy holds - Upside > Base > Downside for net income, EBITDA, and free cash flow, but INVERTED for leverage (Upside < Base < Downside). If that ordering breaks, a scenario input is wired up wrong, not just optimistic or conservative.
