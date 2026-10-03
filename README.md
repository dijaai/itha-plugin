# Itha

Find and compare industrial B2B suppliers from a conversation with Claude.

Itha is a registry of structured seller cards for industrial companies: robots
and automation, machine tools, farm, forestry and construction machinery,
medical and laboratory equipment, drones, marine, components, industrial
software, integrators and distributors. A card is one company's description of
what it sells, in a format built for software to read.

## Use it

Ask for vendors by what you need. For example:

- "Find cobots with at least 10 kg payload and IP65 that are sold in Germany."
- "Which CNC lathe makers have ISO 9001 and serve Germany?"
- "Which distributors carry Universal Robots in Europe?"
- "Why isn't this company on the list?"
- "Where does that payload figure come from?"

For each requirement, Claude reports whether a seller's card states a value
that meets it or does not state one at all. A seller that has not published a
price is reported as price unknown, not as within budget.

## What the results are

Most cards are unclaimed: drafts generated from the company's own public
website and approved by nobody. The page and quoted text behind each fact are
available on request. A card marked verified has been approved fact by fact by
a seller who proved control of the company's domain. Every result says which
it is and links to the card on itha.ai.

Itha does not check the certifications a card lists, and verified is not an
audit.

## What the plugin contains

- A connector to the Itha registry at `https://mcp.itha.ai/mcp`, with five
  read-only tools: search offerings, explain one company against your
  requirements, read a card, show the sources behind a card, and list the
  query vocabulary. It needs no account and no sign-in.
- One skill, `source-vendors`, which tells Claude how to turn a request into
  requirements and how to report what the cards say.

The plugin runs no code on your machine. It is read-only: it does not place
orders, request quotes or contact sellers.

## Data

The plugin sends your search requirements, and the company domains you ask
about, to mcp.itha.ai. It sends nothing else from your conversation or files.
The registry logs each search and each card that is opened, with the calling
application's user agent and a daily-salted hash of the caller's address, and
keeps those logs for 12 months. Do not put anything confidential in a search.
The full policy is at <https://itha.ai/legal/privacy>.

## Support

Report a wrong card at <https://itha.ai/legal/corrections>. For anything else,
write to hello@itha.ai.
