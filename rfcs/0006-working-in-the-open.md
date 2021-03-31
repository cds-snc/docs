---
created-on: 2021-03-31
freshness: 2021-03-31
owner: @dj2
status: proposal
tags:
  - opensource
---

[La version française suit.](#résumé)

# Working in the open
## Summary
CDS as an organization has a commitment to working in the open, inspired by our
peers in the UK, United States, and around the world. As we develop software
products, coding in the open provides a number of important benefits:
 * It encourages good practice
 * It makes collaboration easier
 * External users can help make it better
 * Others can learn from our work
 * It makes it easier to share standards
 * It improves transparency on government’s work
 * It clarifies ownership
 * It helps make government technology seamless
 * It’s easier to start code in the open than to open a closed repository

This RFC attempts to lay out the _how_ of our open source work.


## Motivation
When we collaborate in the open and publish our data publicly, we can improve
Government together. Building services more openly and publishing open data,
simplifies access to government services and information, allows the public to
contribute, and enables reuse by entrepreneurs, nonprofits, other agencies, and
the public.

CDS’s commitment to open source helps to normalize its use and creation across
the Government of Canada. The [GC Digital Standards](https://www.canada.ca/en/government/publicservice/modernizing/government-canada-digital-standards.html)
endorse the use and development of open source software within the Canadian
Government.


## Proposal
* For new development choose a permissive license approved by the Open Source
  Initiative, preferring the MIT License. MIT is a recommended license from the
  [Canadian Government Guide for Publishing Open Source Code](https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/open-source-software/guide-for-publishing-open-source-code.html#toc04) and the licensed used by
  [WET-BOEW](https://github.com/wet-boew/wet-boew).

* When adapting existing code from another organization, understand and respect
  the license terms of the original code. When forking and adapting existing
  projects, refer to the [set of considerations](https://github.com/canada-ca/open-source-logiciel-libre/blob/master/en/guides/using-open-source-software.md#verify-open-source-software-licence) to
  understand and apply license terms and conditions from the GC Office of the
  CIO (OCIO).

* You SHOULD NOT use software or packages that have a non-OSI approved license.

* The [CDS-SNC GitHub organization](https://github.com/cds-snc) is our default
  code repository. If needed or desired by a partner, a similar organization on
  an open code hosting site maybe used.

* For each code repository, publish:
  * A simple and clear code of conduct
  * Contribution guidelines
  * License
  * Security vulnerability disclosure process
  * Issue and PR templates

  Refer to the [repository configuration](https://github.com/cds-snc/.github)
  project for examples to copy.

* Adhere to the Official Languages Act by providing bilingual documentation,
  creating bilingual templates for issues and pull requests.

* Issues opened in an official language MUST be responded to in that official
  language.

* Work to maintain the health of our repositories.
  * Keep your artifacts and repositories clean and accurate.
    * Archive unmaintained repositories
    * Delete stale and merged branches
    * Remove old pull requests that will not be merged
    * Regularly prune old issues.
  * Respond to issues in a timely manner, both internal and external.
  * Respond to PRs in a timely manner. This is especially important if the PR
    won't be accepted for some reason. Make sure it's clear why the PR was
    rejected and if there is anything that could be done to make it acceptable
    in the future.

* Default to open for bug tracking, documentation and project road maps.
  * Providing this information on GitHub (or a public Trello board) makes the
    project more accessible to external (and internal) contributors. It's easier
    to see problems others have encountered and to find ways to start
    contributing.


## Alternatives
The current ad-hoc, undefined approach has served CDS for the last few years.
This model could continue to be used by CDS but has the inherent downside of
causing confusing and differing projects working in differing manners.


---

# Résumé

...