---
created-on: 2021-04-27
freshness: 2021-04-27
owner: @maxneuvians
status: proposal
tags:
  - postmortem
  - incident response
---

[La version française suit.](#résumé)

# CDS Principles for running incident response and doing postmortems

## Summary
Things go wrong. Software breaks. Partnerships aren’t smooth. Delivery takes longer than expected. Sometimes, things go right. In all cases, we should take the time to look back on what happened, how it happened and what we can do better in the future.

Postmortems are a tool for determining what happened, documenting the timelines and discovering what went right and what went wrong. When adopted properly, they help us understand how a given outcome occurred and, if necessary, provide the action items to ensure that outcome doesn’t happen again in the future, thereby strengthening the services delivered.

## Motivation
We need to align as an organisation on the value of postmortems - what they give us, why they are worth investing in, and what the consequences of ignoring outcomes are.

## Proposal

### We acknowledge that people will make mistakes
It is completely unreasonable to expect humans to never make a mistake, otherwise they would never learn. When people make mistakes, we assume they acted with the best intentions based on the information they had at the time. A postmortem needs to honestly and objectively examine the circumstances that led to the fault so we can find the true root cause(s) and mitigate them.

### We will create an environment of psychological safety.
Witnessing the public shaming and blaming of a co-worker for mistakes is a surefire way of reducing the confidence and productivity of others. Future incidences will most likely be covered up and reinforce the blame cycle, leading to more incidents, making the system weaker overall.

### Incidents are an opportunity to learn and reflect
In the broadest sense, an incident is any unplanned work you encounter in your day-to-day operations. Good judgement is required to know when unplanned events require an incident response, as seemingly innocuous events may have terrifying root causes. This will come with experience running incident responses, which means it is better to err on running more than running less. Some examples of events that may trigger the incident process are:

- User-visible downtime or degradation beyond a certain threshold
- Data loss of any kind
- On-call engineer intervention (release rollback, rerouting of traffic, etc.)
- A resolution time above some threshold
- A monitoring failure (which usually implies manual incident discovery)

### We care about the details
It is important to keep an up-to-date timeline of events during an incident as it will be the only moment in time when the information is fresh in your mind. Humans naturally collapse details as time goes by and important nuances will be lost. Similarly, it will give team members joining the incident later on a good overview of where the process is at.

### Action items need ownership and accountability
We can have the best postmortem process in the world, but have it amount to nothing unless we follow up on the action items identified and hold ourselves accountable to them. It is not enough to identify them, they need to be put into backlogs and actioned with dedicated owners. Ideally, postmortems would be shared internally across the organisation (ex. community meetings, Show The Thing) and potentially publicly. We want to demonstrate that we take them and their outcomes seriously. 

### Time needs to be made for incidents and postmortems
The creation, review and completion of postmortems should be given emphasis by the management team. It should be made clear that recording our past successes and failures is a priority. That there is time, and room, for a team to do their postmortem, do them correctly, and follow up as needed.

## Drawbacks
We assume that this is the best way for us to learn from past mistakes and successes. However, it requires significant investment of time and resources to do properly, which comes at the opportunity cost of other work. Should we not properly follow through on our commitments we may end up with a broken process that has wasted time and resources with no usable outcomes.

## Alternatives
Time invested into postmortems could be invested into other work, while incidents are centrally monitored and managed.

## Open Questions
How do these align with the principles of our organisation?

---

# Résumé

...

