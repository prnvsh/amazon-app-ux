# Amazon Checkout Experience: A UX Research Study
<img width="965" height="303" alt="Screenshot 2026-07-13 153105" src="https://github.com/user-attachments/assets/3543d455-c3d7-4c45-88f0-b7458ff58219" />

A mixed-methods UX research project investigating checkout abandonment on a mobile
Amazon-style shopping experience. Built as a functional prototype to test whether
**upfront price visibility** reduces last-moment purchase hesitation.

> **DESG318 Final Project**
> This is an educational prototype. All product data, images, and pricing are
> placeholders. Not affiliated with or endorsed by Amazon.

---

## The Problem

Users reach checkout with clear purchase intent, but abandon at the final step.
Our research asked: *why?*

<img width="625" height="301" alt="Screenshot 2026-07-13 152618" src="https://github.com/user-attachments/assets/b12fde53-bb61-42c0-9a3e-3db359eefa9d" />


> Amazon is losing conversions at the final step of the purchase journey.

---

## Methodology: Triangulation

We converged on this finding using three independent data sources:

| Method | Sample | What it showed |
|---|---|---|
| **Qualitative**, contextual inquiries | 25 users | All reached checkout, all paused before payment, all re-checked info, **none completed purchase** |
| **Quantitative**, survey | ~100 participants | 42.3% compared other products before leaving; 70% cited "not sure about product quality/price" as the reason for abandoning |
| **Behavioral**, in-app session tracking | Live session data | Duration spikes at checkout, repeated scrolling over order summary, multiple interaction events before exit |

**Synthesis:** Users are not abandoning randomly. They are actively re-evaluating
price and product decisions before committing. Checkout functions as a
**decision validation stage**, not a completion stage.

---

## The Experiment

**Design:** N = ~100+ participants, within-subject testing across two variants,
compared against the current (control) experience.

**Metrics tracked:** completion rate, time to completion, interaction intensity
(clicks, scrolls).

### Control: Current Experience
- Price clarity introduced late in the flow
- No support for comparison at checkout
- Observed: high hesitation, frequent backtracking

### Variant A: Upfront Price Visibility
Exposes the final price, including delivery, at the cart stage, before checkout,
so users aren't confronted with new cost information at the point of commitment.
<br>
<img width="655" height="362" alt="Screenshot 2026-07-13 152707" src="https://github.com/user-attachments/assets/25ca1448-76d8-4732-ac9d-06de256618b2" />


### Variant B: Similar Products in Checkout
Surfaces alternative product options inline within the checkout flow, letting
users compare without leaving the funnel.

<img width="659" height="356" alt="Screenshot 2026-07-13 152719" src="https://github.com/user-attachments/assets/defc3284-7c6f-41c0-9a2b-c7b17d13a0de" />

---

## Results

| Variant | Completion Rate |
|---|---|
| Control | 40% |
| **Variant A** (Upfront Price) | **70%** |
| Variant B (Comparison Shelf) | 50% |

- **Variant A** reduced time to completion and showed the strongest lift in
  conversion.
- **Variant B** increased interaction volume and time on page, consistent with
  added cognitive load rather than resolved uncertainty.

<img width="631" height="320" alt="Screenshot 2026-07-13 152748" src="https://github.com/user-attachments/assets/951258f7-fef2-4d01-ae28-4f045d3ef1ae" />

---

## Recommendation

Prioritize price clarity at the point of commitment to reduce abandonment at
scale. Variant A (upfront price visibility) is the stronger candidate for
further testing.

**For the business:** faster transactions, fewer drop-offs, more value
extracted from existing traffic.
**For the customer:** no last-minute pricing surprises, faster and more
confident decisions.

**Next steps:** re-run with a larger sample to confirm significance; consider
combining upfront pricing with a lighter-weight comparison affordance that
doesn't add checkout friction.

---

## Project Structure

```
├── assets/
│   ├── css/styles.css       # Application styles
│   └── js/app.js            # Application logic, product data, session tracking
├── img/                     # Product images (placeholder assets)
├── index-a.html             # Control experience
├── index-b.html             # Variant A: upfront price visibility
├── index-c.html             # Variant B: comparison shelf in checkout
├── PROJECT_SUMMARY.md
└── skill.md
```

---

## Tech Stack

- HTML5, CSS3 (Flexbox/Grid), vanilla JavaScript (ES6+)
- Google Fonts (Roboto)
- Session/interaction tracking via a lightweight event-capture module,
  beaconed to a Google Apps Script endpoint for analysis
- No frameworks, no build step. Open any `index-*.html` directly in a browser

---

## Running Locally

```bash
# Python
python -m http.server 8000

# Node.js
npx serve .
```

Then open `index-a.html` (control), `index-b.html` (Variant A), or
`index-c.html` (Variant B) in your browser.

---
