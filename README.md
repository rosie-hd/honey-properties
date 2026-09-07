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
