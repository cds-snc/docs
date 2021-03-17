[La version française suit.](#TODO)

# CDS-SNC Request for Comments

This repository is the source of truth for development practices at CDS. The
idea is modeled after the
[GOV.UK RFC Repository](https://github.com/alphagov/govuk-rfcs)
with the intent to provide a single location for the discussion and 
documentation of technical decisions. As with the GDS model, this repository is
open for the benefit of other governmental teams.

For those not familiar with ‘Request For Comments’ (RFC), we will *loosely*
follow the principles as described here,
https://en.wikipedia.org/wiki/Request_for_Comments.

## Process
1. Create a branch and copy the [rfc-template.md](rfc-template.md)
to `rfcs/0000-my-proposal.md` and edit as needed. The RFC can be authored in
either official language, but must be translated be being accepted. A rejected
RFC does not need to be translated.
2. Images and other files should be placed in a `rfcs/0000-data` folder.
3. Create a pull request against this repository.
4. Rename the `0000` in your RFC file and directory to match the PR number (please keep the leading zeros). Push the renamed files to the branch.
5. Post a link in the #devz-cds slack channel. Feel free to @mention specific
people if their review is desired.
6. Set the assignee for the PR to yourself.
7. Make changes as needed based on the reviews.
8. Push the PR forward. If needed, talk with your tech lead to determine who
needs to review the PR or how to get it unstuck.
9. a) If rough consensus is achieved and approval has been marked in the PR
      squash and merge the change into the repository.
   b) If the PR was rejected, record the reasons in a final comment and close 
      the PR.

## Maintaining RFCs
In most cases, RFCs should be replaced by new RFCs instead of being edited.
When an RFC is obsolete it should be moved into the `rfcs/archive` folder
as part of the PR creating the new RFC. The obsolete RFC should have 
metadata added into the YAML front matter stating:

```yaml
---
obsoleted-by: 0001-my-new-proposal.md
obsoleted-date: 2021-02-23
---
```

The new RFC should have a YAML front matter entry listing the obsolete RFC:

```yaml
---
obsoletes: 0000-my-proposal.md
---
```

## Contact

For questions or feedback, you can email the Canadian Digital Service at
[cds-snc@tbs-sct.gc.ca](mailto:cds-snc@tbs-sct.gc.ca) or
[create an issue](https://github.com/cds-snc/cds-snc-rfcs/issues)
in this repository.

----

# Translate .....