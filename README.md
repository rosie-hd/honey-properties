# Honey Properties

A single-file underwriting dashboard for buy-and-fit-out property deals, and the
five-year plan they add up to.

## Pages

- **Deal** — one worked example, start to finish, in the order you would think about
  it: buy at the bottom of what the area trades at, spend, sell at the top, then the
  same again with extra floor area built. Every figure is editable.
- **Properties** — every deal on the shelf; click one to open its full model.
- **Markets** — where the widest period-property spreads are in the UK, with every price
  level labelled for where it came from. Click a market to load its range into the deal.
- **5-year plan** — the profit target, the ramp towards it, and where the money is today.

## The plan

The target is a net profit a year, reached as fast as the capital allows. With a 100%
return, profit on a project equals the equity put into it — so the target does not set
the pace. What sets it is the capital you start with, how long a project takes start to
exit, how many you can run at once, and how much profit goes back in. Those four are on
the page and everything re-simulates as you move them.

The simulation runs month by month for five years: capital is deployed as fast as it
exists and as fast as projects can be taken on, each returns after its period, and the
reinvested share goes straight back out. Because a project takes years, profit lands in
lumps rather than evenly, so the plan is judged on the **run rate** — cumulative profit
over years elapsed — not on whether one lucky year clears the bar.

Actual cash in and cash back are recorded per property and drive the totals.

Open `index.html` in any browser — there is no build step and no server.

## What it models

A trade, not an income asset. Buy for X, spend X on it, sell for X, X months later —
am I making or losing money?

- **Money in.** Purchase, buying costs, works plus contingency, and the interest that
  runs the whole time you hold it, paid monthly or rolled up into the loan.
- **Two debt tranches, priced separately.** The building is borrowed against from day
  one; the works facility is drawn down as the job runs and sits fully drawn until sale.
- **Money back.** Sale price as a rate or a total, less selling costs, less the loan.
- **The answer.** Profit, return on the cash you put in, and that return compounded to
  a year so an eleven-month job and a three-year one can be compared.
- **Price per sq ft** for the subject against comparable sales.

## Buildings or land

Area is held in square feet internally but entered and read back in **sq ft, acres or
hectares**. Every per-unit figure follows — purchase, all-in cost, revenue, the exit,
and the comparable-sales spread. Quoting a Cairngorms forestry block at four pence a
square foot is not a figure anyone would use.

## Many properties

The page opens on a shelf of every property you have modelled, each card carrying its
cash in, IRR, purchase price, all-in price per sq ft and a sparkline of the annual cash
flows. Click one to open it, "All properties" to come back. Properties can be duplicated
(handy for testing a variant of the same deal) and deleted. Each carries its own
assumptions and its own comparable sales.

A single deal saved by an earlier version is migrated onto the shelf on first load.

## Reading a listing

Drop a **brochure or a printed listing PDF** on the panel at the top and it pulls out
the asking price, the floor area, the property name and the listing URL, showing the
sentence each figure came from. Nothing is applied until you click; nothing is
uploaded — the file is parsed in your browser.

Pasting the listing text is the most reliable route of all. Screenshots are read with
OCR as a best effort: clean screenshots of text usually work, floorplans often do not.

Areas quoted in square metres are converted. A row labelled NIA wins over a larger
GIA total, because the model underwrites net internal area. Figures on a "per annum",
"pcm", "per sq ft", "service charge" or "stamp duty" line are never mistaken for the
asking price.

## Opening a deal from a link

Any input can be set from the query string, so a property can be handed over as a
single URL instead of a list of figures to retype:

    ?name=1+Osberton+Road&link=https://…&ccy=%C2%A3&purchase=895000&sqft=958

Values that arrive this way are listed in a banner on the page — a number you did not
type is one you should get to check — and anything outside a field's range is capped,
and says so.

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
