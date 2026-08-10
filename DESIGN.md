# Tip Calculator

## Product

A fast, simple and mobile-first tip calculator for restaurant bills in the United States.

## Problem

A user at a restaurant wants to quickly answer:

- How much should I tip?
- What is my total bill?
- How much does each person pay?

The user should be able to get the answer within a few seconds.

## Product principles

- Extremely simple
- Mobile-first
- No signup
- No backend
- No ads in the MVP
- No tracking
- Everything calculated locally in the browser
- No unnecessary steps
- No "Calculate" button
- Results update immediately

## MVP

### Bill

- Bill amount input
- Mobile-friendly numeric input

### Tip

Provide quick-select buttons:

- 15%
- 18%
- 20%
- 25%
- Custom

20% should be the default.

### Split

- Number of people
- Default: 1
- Plus/minus stepper
- Show amount each person pays

### Results

Clearly display:

- Amount each person pays
- Total bill
- Tip amount

The per-person amount should be the most prominent result when the bill is split.

## Themes

- Dark mode is the default.
- A clear light/dark toggle is always available.
- Store a deliberate user choice in localStorage and apply it before first paint to prevent theme flash.
- Both themes must remain high-contrast and polished.

## Tip

Provide quick-select buttons:

- 15%
- 18%
- 20%
- 25%
- Custom

Custom mode is a distinct state: no preset remains selected. It combines a smooth percentage slider with a numeric input for precise values, including decimals such as 17.5%.

## Rounding and splits

- Keep “Round each person's share up” visible in the primary calculator UI, but visually secondary to bill, tip, and split inputs.
- Its off state should be quiet but legible.
- When enabled, state the rounded amount each person pays and the additional amount collected across the table.
- When equal splitting produces fractions of a cent, do not show a single rounded figure as if everyone pays it. Show a transparent cent-balanced split (for example, 2 people pay $39.17 and 1 pays $39.16) that adds exactly to the total.
- Never hide rounding adjustments.

## More options

Keep less-common settings behind a collapsed "More options" section.

Options should include:

- Service charge already included

These should not clutter the main calculator.

## Sharing

Allow the user to quickly copy/share the result.

Example:

"$22.00 each, including $11.00 tip"

## UX goals

The calculator should feel faster and simpler than existing competitors.

Avoid:

- unnecessary forms
- large amounts of explanatory text
- unnecessary charts
- account creation
- popups
- complicated settings
- unnecessary animations

## Competitor research

Competitors researched include:

- Calculator.net
- TipCalculator.org
- TheTipCalc
- CalculateThis
- MAJC
- USTipCalc

The competitors provide many useful features, but some introduce additional controls, explanations and options before the user gets their answer.

Our differentiation is not having the most features.

Our differentiation is:

**Fast + simple + clear.**

## Future possibilities

Do not implement these in the MVP:

- Receipt scanning
- Itemized bill splitting
- Multiple currencies
- Country-specific tipping databases
- Saved history
- Accounts
- Advanced analytics
- Charts
- Travel guides
- Large SEO content sections

These can be considered later if they prove useful.

## Technical direction

- Astro
- Client-side JavaScript
- No database
- No authentication
- No backend required for calculations
- Responsive design
