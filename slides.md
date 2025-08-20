# Agenda
- Performance Snapshot <!-- .element: class="fragment" -->
- Revenue & EPS Drivers <!-- .element: class="fragment" -->
- Outlook & Guidance <!-- .element: class="fragment" -->
- Q&A <!-- .element: class="fragment" -->
Note:
Keep this high-level; details are on later slides. Fragments reveal one by one. 

---

## Performance Snapshot (Q3)
**Revenue:** \$3.42B  •  **EPS (diluted):** \$1.28  
**YoY Growth:** 12% <!-- .element: class="fragment" -->
**Operating Margin:** 24% <!-- .element: class="fragment" -->
Note:
Call out YoY and margin expansion; tie to cost discipline.

---

## Revenue Bridge (illustrative)
1. Base Q2 run-rate <!-- .element: class="fragment" -->
2. Seasonal uplift (retail) <!-- .element: class="fragment" -->
3. Interest income tailwind <!-- .element: class="fragment" -->
4. FX headwinds <!-- .element: class="fragment" -->
Note:
Use each fragment to discuss sequential changes.

---

## Financial Formulae
- **Compound growth:** $FV = PV \cdot (1+r)^n$  
- **Weighted Avg. Cost of Capital (WACC):**  
  $WACC = \\frac{E}{V}R_e + \\frac{D}{V}R_d(1-T)$
- **Black–Scholes (call, sketch):**  
  $C = S_0 N(d_1) - K e^{-rT} N(d_2)$
Note:
Keep equations visible while you summarize intuition behind each.

---

## Sample Code (data prep)
```python
import pandas as pd

df = (pd.read_csv("q3.csv")
        .assign(growth=lambda d: d.revenue.pct_change())
        .query("segment != 'Legacy'"))
print(df.describe())
