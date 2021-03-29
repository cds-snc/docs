---
created-on: 2021-03-29
freshness: 2021-03-29
owner: @dj2
status: draft
---

[La version française suit.](#résumé)

# RFC Process

## Summary
This RFC lays out some foundations for the RFC process, mostly around
the approval and acceptance process.

## Motivation
Without some sort of framework it is difficult to know how the RFC
process is going to work and to align everyone in the same direction.
There are questions around when approvals are needed, how many, how long
do we wait. This RFC attempts to set some guard rails for this process
and to start us in the right direction.

## Proposal
1. A proposal, from PR announcement to commit MUST be no less then 2 weeks.
   The announcement MUST be in Slack on the appropriate channels for the
   RFC content.
2. An RFC MUST have approval to commit. An RFC needs approval from the
   communities which will be affected by the RFC (or, a best guess as to
   the impacted communities).
   (i.e. an RFC to setup base labels needs Dev, SRE and PM approval as
   all three communities will need to agree)
3. If there is someone uniquely positioned to review the RFC that user
   MUST be added for approval, this may extend the wait period outside
   the 2 weeks if the required approver is on vacation or leave.

## Drawbacks
Adding too much process will make the RFC process more heavy weight.
We'd like the whole system to be as light as possible, but still be
usable by the community. Adding too many rules may sway folks off
creating/maintaining RFCs.

## Alternatives
One alternative for the approval is to have the head of a given
community be required for approval. This adds an extra layer of
management, and provides a bit more weight to the RFC but also adds a
substantial block in terms of community head time. As a first pass, I
think we should wait before putting that block in place to see if there
is uptake of the RFC process in the communities.

---

# Résumé

...
