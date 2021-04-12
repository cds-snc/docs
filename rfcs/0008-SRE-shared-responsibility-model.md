---
created-on: 2021-04-12
freshness: 2021-04-12
owner: @maxneuvians
status: proposal
---

[La version française suit.](#résumé)

# Site reliability engineering (SRE) shared responsibility model

## Summary
At the core of site reliability engineering is the idea that operations and
product teams share ownership by using the same tools and techniques across
the technology stack. However, we still need to define the boundaries of
ownership so we know which team is responsible for which task.

## Motivation
Delineating responsibility, and acknowledging that it is ultimately shared,
will help facilitate communication and smooth operations between the site
reliability engineering team at CDS and the product teams across business units.

## Proposal
In our shared responsibility model, the SRE Team is responsible for:
- Life cycle management of AWS accounts including: provisioning, granting access to product team members, and ensuring that the [Landing Zone](https://aws.amazon.com/solutions/implementations/aws-landing-zone/) is configured properly.
- Providing evidence for security assessments of core infrastructure components (ex. [Landing Zone](https://aws.amazon.com/solutions/implementations/aws-landing-zone/) components)
- Maintaining any tooling that is developed by the SRE Team (ex. Custom GitHub integrations, [Secret](https://github.com/cds-snc/secret), [CDS Wide load testing tools](https://load-testing.cdssandbox.xyz/)) which are used by product teams.
- Help surface security issues for product teams to act upon
- Recommending best practices for GitHub and AWS

In our shared responsibility model, product teams are responsible for -

- through the development community:
    - Setting up their own operations inside AWS accounts using best practices such as infrastructure as code
    - Building continuous integration / continuous delivery pipelines
    - Follow best practices for Github and AWS as articulated by the SRE team

- through the delivery management community:
    - Completing their own security assessments with some evidence provided by the SRE team

- through the product management community:
    - Resolving security issues inside the infrastructure or application (unless they are
    [Landing Zone](https://aws.amazon.com/solutions/implementations/aws-landing-zone/) specific)

## Drawbacks
Keeping a set of shared responsibilities, short, high level, and clear comes at the cost
of muddled ownership when pertaining to very specific issues or concerns. Security specifically
will fall prey to this as both parties may assume the other is responsible, or the team responsible
is under-qualified in dealing with the issue. The only solution is clear and regular communication
between all parties and willingness to lend a hand instead of pushing the problem back.

## Alternatives
Returning to a more traditional approach where artifacts are handed from the development team to be deployed and run by an operation team.

## Open Questions
- How often is this shared responsibility model reviewed?
- How arbitrates disputes and who has the final authority on decisions?

---

# Résumé
The translated version will go here if the RFC is accepted.