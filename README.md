# Ticket Fairy event planning skills

Plan an event, prepare its tickets and team, book artists and travel, and build the running order.

Official [Ticket Fairy](https://www.ticketfairy.com) agent skills, selected from the
[canonical collection](https://github.com/theticketfairy/agent-skills). Install this collection or the individual skills you
need; their names and instructions are the same in both repositories.

## Install

```sh
npx skills add theticketfairy/event-planning-skills
```

List the available skills without installing:

```sh
npx skills add theticketfairy/event-planning-skills --list
```

Or select one skill:

```sh
npx skills add theticketfairy/event-planning-skills --skill start-organising-events
```

The current Skills CLI requires Node.js 22.20 or later. Skills install to your
current project by default. Choose the supported agent in the CLI. See the [Skills CLI documentation](https://skills.sh/docs/cli).

## Skills

| Skill | When to use it |
| --- | --- |
| [`start-organising-events`](skills/start-organising-events/SKILL.md) | Help an organiser start a Ticket Fairy workspace for ticketing or standalone event management, prepare their first event and compare published feature plans. |
| [`set-up-event-tickets`](skills/set-up-event-tickets/SKILL.md) | Set up a Ticket Fairy event: ticket types, release tiers, sessions, seating, resale and transfer rules. Use when an event organiser wants to create or change the tickets their event sells. |
| [`follow-event-type-playbooks`](skills/follow-event-type-playbooks/SKILL.md) | Follow the Ticket Fairy order of work for festivals, club nights, tours, conferences and other event types. Use when an organiser plans a whole event of one type. |
| [`run-event-workflows`](skills/run-event-workflows/SKILL.md) | Follow Ticket Fairy start-to-finish workflows: on-sale day, repeating last year's event, and changing plans. Use when an organiser faces one of these moments. |
| [`sell-passes-and-extras`](skills/sell-passes-and-extras/SKILL.md) | Sell Ticket Fairy extras beyond a single event ticket: add-ons sold with tickets, VIP tables and bottle service, hotel rooms and travel for your ticket buyers, and one pass that covers several of your events. Use when an event organiser wants to sell an add-on, a table, a stay or a pass. |
| [`manage-venue-pages`](skills/manage-venue-pages/SKILL.md) | Claim a Ticket Fairy venue page and keep its details current. Use when a venue team wants to control what people read about their venue. |
| [`manage-brand-and-team`](skills/manage-brand-and-team/SKILL.md) | Manage a Ticket Fairy brand kit, team roles, several brands, collectives and account security. Use when an organiser wants to add people, change roles or organise brands. |
| [`book-and-advance-artists`](skills/book-and-advance-artists/SKILL.md) | Hold dates, make offers, send contracts, collect riders, advance performers and settle shows in Ticket Fairy. Use when an organiser books artists or speakers for an event. |
| [`book-hotels-and-travel-for-the-team`](skills/book-hotels-and-travel-for-the-team/SKILL.md) | Hold hotel rooms, share rooming lists, plan pickups and book travel for artists and crew in Ticket Fairy. Use when an organiser looks after where the team stays and how it travels. |
| [`plan-the-running-order-and-show-day`](skills/plan-the-running-order-and-show-day/SKILL.md) | Build the running order and run of show, check clashes, share day sheets and call the show live in Ticket Fairy. Use when an organiser plans set times or runs show day. |

## Authority and recovery

A skill grants no account permission and does not authorise sending messages,
creating tickets, refunding orders or taking payment. Keep each action within the
person's approved scope and current role. Buyer discovery is public and read-only;
buyer purchases use a separately supported handler and explicit approval of the
final tickets, total and currency, or continue in the official browser checkout.
Organiser credentials do not grant purchase authority. Keep credentials out of chat
and logs. After an uncertain change, recover its original result before
retrying; never issue a new refund, send or ticket grant to resolve uncertainty.

## Documentation and maintenance

- [Official guides](https://www.ticketfairy.com/guides), read live with the public
  [guides MCP server](https://www.ticketfairy.com/docs/mcp).
- [Developer documentation](https://www.ticketfairy.com/developers).
- [Published skill index](https://www.ticketfairy.com/.well-known/agent-skills/index.json).
- [Agent rules](AGENTS.md) and [canonical source](https://github.com/theticketfairy/agent-skills).

`SOURCE.json` records the canonical revision and skill hashes. Make instruction
changes in the canonical repository, then use its
`scripts/build_skill_repositories.py` to copy the reviewed release into this
repository. Do not maintain an independent fork of a skill here.

GitHub publication does not prove skills.sh indexing. Its
[FAQ](https://skills.sh/docs/faq) describes automatic listing through anonymous
Skills CLI installation telemetry. No installation count or indexing status is
claimed by this repository.

## Licence

MIT. See [LICENSE](LICENSE).
