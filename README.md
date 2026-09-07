# Honey Properties

A single-file underwriting dashboard for buy-and-fit-out property deals.

Open `index.html` in any browser — there is no build step and no server.

## What it models

- **Two debt tranches, priced separately.** Leverage on the purchase price and on the
  fit-out are set independently, at their own interest rates, plus interest accruing
  over the build period before income starts.
- **Total cash in.** Purchase + acquisition costs + fit-out + contingency + build
  interest, less all debt drawn.
- **Return on that cash, every year of the hold** — as a cash figure and as
  cash-on-cash %, alongside IRR, equity multiple, DSCR and yield on cost.
- **Exit.** Forward NOI capitalised at an exit cap rate, less sale costs and the
  outstanding loan balance.
- **Price per sq ft** for the subject property against a spread of comparable sales,
  filtered by size, distance and recency.

## Using it

Each deal carries a **listing link** at the top, kept alongside the assumptions so the
numbers always point back at their source. The page does not read the listing — a
static file in a browser cannot fetch another site, and the portals block it anyway —
so the figures stay yours to enter.

Every figure is editable three ways: drag it sideways, scroll the wheel over it, or
click and type. Shift for 10x steps, Alt for fine ones. Everything recalculates live
and saves to your browser.

Comparable sales are typed or pasted in (address, sq ft, price, date, distance in
miles) — there is no market data feed. The rows it ships with are illustrative
placeholders, not real sales.

Nothing here is investment advice; every number is an assumption you set.
