---
created-on: 2021-03-23
freshness: YYYY-MM-DD
owner: @CalvinR
status: draft
tags:
  - github
  - project_management
---

[La version française suit.](#résumé)

# CDS Github Label Standard

## Summary
Create an organization wide standard for Github labels to ensure a consistent way of identifying issues across the org as well as allow customization of labels to happen at the business unit level.

## Motivation

Currently every github repo has to modify existing Github labels upon creation of a new repo or use the default labels. Unfortunately GH does not provide bilingual labels out of the box and so we are non-compliant with OLA (Official Languages Act) requirements. If we customize labels for a business unit (BU) we will then have to manually copy labels into every repo that is owned by that BU.

## Proposal
A standard baseline of labels to be applied across the cds-snc github organization. This standard will be enforced through a github action on each repo, and will allow for a consistent way to identify issues across the organization and will allow for products, business units or specific products to extend this baseline with labels that fit their needs. This will also allow for CDS to ensure that we are respecting our requirements to communicate with people in their official language of choice.

See https://github.com/cds-snc/covid-alert-server-labels for an example of what is being proposed to implement this solution. 

The source of truth for these labels will reside in github and what is put forth in this document is just to start the discussion. The understanding is that if this Standard is accepted that a github action for syncing labels in a project will be created that will be created in github and maintenance and discussion will continue in those repositories. 

### Baseline Labels
This list of labels will be standardized across the organization and will be mandatory, they will apply high level groupings and statuses and will allow for a consistent way of talking about issues across projects.

This consistent vocabulary will enable us to create reporting tools that can be applied to any project using the system and will provide a consistent view into the state of all CDS products. It should also reduce cognitive burden when onboarding to the project. 

The list of proposed baseline labels can be seen in Appendix A

### Product Specific Labels

Each product will be allowed to apply their own unique set of labels alongside the baseline labels. 


```yaml
- Name: High Priority | Haute priorité
  Description: 
  Colour: 
- Name: Medium Priority  | Priorité moyenne
  Description:
  Colour:
- Name: Low Priority | Faible priorité
  Description:
  Colour
- Name: Bug | Bogue
  Description:
  Colour:
- Name: Documentation
  Description:
  Colour:
- Name: Security | Sécurité
  Description:
  Colour:
- Name: Privacy | Vie privée
  Description:
  Colour:
- Name: Wont fix | Ne résoudra pas
  Description:
  Colour:
```


### Label Requirements

Every label is bound by the following requirement:  

- A label must be bilingual in the format `en | fr`
- A label must not use a colour used by a baseline label

It is recommended that labels make sense for the product/project they are being applied to and that they are not relevant to only a very small number of issues but this isn’t mandatory.

### Governance

Governance surrounding labels will occur in Github repos, as labels are defined as json objects and are enforced through Github actions we can use Github to apply a level of lightweight automated workflows. Github's Code owner functionality will be used to manage approvals from owners.

#### Creation, Modification, and Approval
Label Meta-data is defined by Github and can be found here https://docs.github.com/en/rest/reference/issues#create-a-label

The governance surrounding the creation, modification and approval of labels will depend on what label group is being acted upon. 

**CDS wide labels** will be owned by the head of product management. 

**Product Specific Labels** will be owned by the product manager, this is done by applying a .codeowner file against the labels.js file.
Github Pull requests can be used to provide a lightweight and transparent approval process. 

Any employee of CDS can open a PR or Issue updating the labels, it is recommended that these are documented with a rationale for change.

#### Github Actions
The head of SRE will own the CDS label repo minus the label.js file which is owned by product managers.

Product specific label repos will be owned by the business unit’s SRE member or the teams 

## Drawbacks
CDS Employees are not used to things being dictated from top down so this has a potential to cause friction with employees who are used to doing what they want.

## Alternatives

One alternative is that we continue on with business as usual where each product has a mix of the default github labels and ad-hoc project labels their own labels and will need to set things up from scratch each time. This potentially means an increase in cognitive load when switching between projects and also makes it hard to report up on issues in projects.

---

# Résumé

...
