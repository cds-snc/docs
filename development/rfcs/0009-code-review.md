---
created-on: 2021-04-27
freshness: 2021-04-27
owner: @dj2
status: proposal
tags:
  - software development
  - practices
---

[La version française suit.](#résumé)

# Code Review

## Summary
Code review is an integral part of how we work at CDS. Having your code
reviewed provides an extra layer of experience and guidance. It's easy to
get lost in the forest and miss potential complications and
simplifications.  Providing reviews gives the opportunity to understand
and shape the system as a whole.

The process on both sides allows our developers to learn from each other.
As much can be learned by the reviewer as the reviewee.

This RFC lays out considerations for reviewing code at CDS.

## Motivation
A shared set of considerations helps ease both the burden of being
reviewed and that of being the reviewer. Code review is inherently
subjective, different reviewers focus on different things. This can make
the review system seem opaque. Shared considerations help to ease that
subjectivity by giving guide rails to make reviews more consistent.

## Proposal
Below is a list of considerations these are divided into principles and
technical consideration. Focus on the principles and then lead into the
technical considerations.

### General guidelines
 - Code reviews are required at CDS.
   - Each review should have a technical reviewer.
   - Add Design, Research, Product Management, Service Owner, as needed.
 - Tend towards questions rather then statements.
   - The reviewer may not understand all the considerations a reviewee
     put into the code.
   - The reviewee may not understand the reviewers past experience with
     the code.
 - [Be nice](https://qz.com/work/625870/after-years-of-intensive-analysis-google-discovers-the-key-to-good-teamwork-is-being-nice/)
   - Read the CDS [Code of Conduct](https://github.com/cds-snc/.github/blob/master/CODE_OF_CONDUCT.md)
 - Escalate if the review is blocked.
   - The goal of the review is that the code looks good to the reviewer.
     It doesn't have to be perfect, it doesn't have to be how the
     reviewer would write it. Just, good.
   - The term good is intentionally vague as it depends on context. As a
     guide, follow the [Technical
     Considerations](#technical-considerations) listed later in this
     document.
 - In general authors should merge their own PRs.
   - This allows them to make any final touch ups or edit the commit
     message.
   - Using merge commits ends up with the person pressing the merge button as
     the author in GitHub and makes the authorship harder to understand.
 - Cleanup branches after merge. If possible, enable the auto-delete
   after merge option on repositories.
 - Prefer to `Squash and merge` commits.
   - The development history is in the PR if desired, but typically
     doesn't add much to the main repository.
 - Force pushing to a repo should be a last resort.

### Principles for reviewees
 - The title and description should provide all the needed context.
   - The PR will serve as a record of the change into the future.
   - Anything important for the reviewer to know (other approaches tried,
     testing you’ve done, etc) is worth including.
   - Link to any associated issues or Trello cards.
   - If the PR is broken apart to make review easier, explain how it was
     broken apart and include the next steps in the PR description.
   - List any steps, caveats or gotchas that the reviewer will need to
     know.
 - Do your best to address all comments (even just to say "Done" or put
   in a thumbs up).
   - Marking the comments as `Resolved` makes it easier to understand
     what still needs to be done.
 - Assume the best intention from review comments
 - Wait for the tests to pass before you merge.
 - Tend towards smaller changes. They are easier to understand and
   faster to review.


### Principles for reviewers
 - Try to comment on the PR in as short an interval is possible (<24
   hours preferably, excluding weekends).
   - The comment doesn't have to be the review, but can just be a
     comment letting the reviewee know when you'll be able to review.
     This gives them the opportunity to find another reviewer if needed.
   - If you’re not sure how someone wants their code reviewed or how they
     prefer to receive feedback, talk to them beforehand.
 - Point out when something is particularly good or clever.
   - Reviews often focus on the negative so highlight the good as well
     when you see it.
 - Be explicit.
   - Include screenshots or gifs if they help make your point.
 - Programming is subjective.
   - Different approaches are valid.
   - Ask for clarifications if you need any.
 - Communicate which ideas you feel strongly about and those you don't.


### Technical Considerations

#### Logic
 - Does the code work?
   - Does it perform its intended function?
   - Is the logic correct?
   - Is the proposed UI accessible?
 - Does this the change introduce tech debt?
   - Adding tech debt isn't a bad thing, but we need to make sure we understand
     why we're adding it and how we're going to contain it.
   - If adding, are there comments or documentation around the debt so future
     maintainers can understand the issues?
 - Does this change introduce any security concerns?
   - Does it accept or handle user data?
   - Does the ATO or other security documentation need to be updated?
 - Is all the code easily understood?
   - Which parts are confusing to you and why?
   - If you are taking a lot of time to understand the code, perhaps it
     needs comments or refactoring.
 - Can the code be simplified?
   - Write the code you need, not the code you may need.
 - Does similar functionality already exist in the codebase?
   - If so, why isn't this functionality reused?
     (Note: it's okay to not reuse -— but it's worth asking the question.)
 - Does the code follow the format/style of the surrounding code?
   - In general, this means applying the appropriate code formatter for
     the repository. In the case there is no formatter, follow the
     surrounding style of the code being modified.

#### Comments
 - Has all commented-out code been deleted?
   - We can find past code using version control if needed.
 - Are all functions commented?
 - Do comments exist to describe the intent of any thorny logic?
 - Are there comments that no longer make sense?

#### Errors
 - Can you think of any use case in which the code does not behave as
   intended?
 - Are potential errors being caught and logged?
 - Are third-party utilities used which may return errors?
 - Is any unusual behavior or edge-case handling described?

#### Tests
 - Do tests exist, and are they comprehensive, covering good input, bad
   input and errors?
 - Are tests checking at the right level?
 - Do the existing set of tests pass?
 - If there is an instance created for the PR has the functionality been tested
   through the UI?


#### Documentation
 - Does this change require an update to the README or configuration
   files?
   - Are there internal documents which need to be updated?
 - Is the reason for the change outlined in the commit message?


## Drawbacks
Making the code review process too restrictive makes it more of a chore
then it should be. We want the process to be fairly light, but still
maintain value.


## Alternatives
Without guide rails the process could continue as is. Different styles of
code review being provided by different folks. While functional, this
style can be difficult. If you need multiple reviewers it's easy to
get conflicting advice. This can also cause reviewees to use their
favourite reviewers, pushing the review load onto a limited number of
people.

## Further references

The Government Digital Service in the UK has really good guidance around
pull requests.
 1. [Pull request guidance](https://github.com/alphagov/styleguides/blob/master/pull-requests.md)
 2. [Writing a good commit message](https://github.com/alphagov/styleguides/blob/master/git.md)

[Code Review guidelines for reviewers and reviewees](https://github.com/thoughtbot/guides/tree/master/code-review)
by thoughtbot is terrific.


---

# Résumé

...




