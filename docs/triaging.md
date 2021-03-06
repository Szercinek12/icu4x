Issue Triaging
==============

ICU4X uses GitHub for tracking feature requests and work items.

- All issues should have a type label.
    - [Query: issues needing a type](https://github.com/unicode-org/icu4x/issues?q=is%3Aissue+-label%3AT-bug+-label%3AT-core+-label%3AT-docs+-label%3AT-enhancement+-label%3AT-invalid+-label%3AT-question+-label%3AT-task+-label%3AT-tests)
- All valid issues should have a component label.
    - [Query: issues needing a component](https://github.com/unicode-org/icu4x/issues?q=is%3Aissue+-label%3AC-data+-label%3AC-datetime+-label%3AC-locale+-label%3AC-meta+-label%3AC-numbers+-label%3AC-process+-label%3AC-test-infra+-label%3AC-unicode+-label%3AT-invalid+)
- All *open* or *backlog* issues should have an assignee or **help wanted** label.
    - [Query: open issues needing assignee or help wanted](https://github.com/unicode-org/icu4x/issues?q=is%3Aissue+is%3Aopen+-label%3A%22help+wanted%22+no%3Aassignee)
    - [Query: backlog issues needing assignee or help wanted](https://github.com/unicode-org/icu4x/issues?q=is%3Aissue+is%3Aclosed+label%3Abacklog+-label%3A%22help+wanted%22+no%3Aassignee)
- All valid *closed* issues should have a resolution, linked pull request, or the **question** or **task** type.
    - [Query: closed issues needing resolution or linked PR](https://github.com/unicode-org/icu4x/issues?q=is%3Aissue+is%3Aclosed+-linked%3Apr+-label%3Abacklog+-label%3AR-duplicate+-label%3AR-needs-more-info+-label%3AR-obsolete+-label%3AR-out-of-scope+-label%3AT-question+-label%3AT-invalid+-label%3AT-task+)
- If an issue is open, the issue should be actionable. Open issues should generally have an activity update once every 60 days.
    - [Query: least recently updated open issues](https://github.com/unicode-org/icu4x/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-asc)
- If an issue is unresolved but lower-priority or not immediately actionable, it should get the **backlog** label and be closed.  The backlog should be checked periodically for issues that should be reopened.
    - [Query: most recently updated backlog issues](https://github.com/unicode-org/icu4x/issues?q=is%3Aissue+is%3Aclosed+label%3Abacklog+sort%3Aupdated-desc)

## Fields

### Type

Labels starting with `T-` are *type* labels, indicating the type of deliverable for the issue.  Every issue should have one:

- **T-bug** = a defect in existing code.
- **T-core** = a high-priority improvement or new feature.
- **T-docs** = relates to documentation, including user guide, architecture design, team processes, and API docs.
- **T-enhancement** = a lower-priority improvement or new feature.
- **T-invalid** = spam, etc.
- **T-question** = an issue that can be addressed in the discussion thread without checking in any code or documentation.
- **T-task** = a task, not a code change.
- **T-tests** = the issue can be addressed by unit testing.

### Component

Labels starting with `C-` are *component* labels, indicating the functional component for the issue.  Every issue should have one:

- **C-data** = related to data pipeline components.  Note: issues relating to data specific to a different component should use the more specific component.
- **C-locale** = related to locale-related components.
- **C-meta** = not specific to one specific component; affects ICU4X as a whole.
- **C-process** = related to team processes, but not ICU4X code.
- **C-test-infra** = related to integration test infrastructure components.  Note: issues relating to tests specific to a different component should use the more specific component (and can use the `T-tests` issue type).

### Assignee

The assignee is the user who is *accountable* for the issue: tracking its progress, obtaining the necessary approvals, and so forth.  The assignee is often the same as the reporter.  The assignee is not necesarilly the same as the user who is *responsible* for writing the necessary code fixes.  Users interested in being *informed* or *consulted* can subscribe to the issue.

For more on the difference between *responsible*, *accountable*, *consulted*, and *informed*, see the [RACI Matrix](https://en.wikipedia.org/wiki/Responsibility_assignment_matrix).

An issue may have the **help wanted** label if there is no assignee.

### Resolution

All *closed* issues should have either (1) the "question" type, (2) a linked pull request, or (3) one of the following labels:

- **backlog** = the issue is not fixed, but it could be revisited in the future.
- **R-duplicate** = the issue is a duplicate of some other issue.
- **R-needs-more-info** = the issue might be valid, but the subcommittee either does not understand the issue or was unable to reproduce it.  The reporter should provide more information.
- **R-obsolete** = the issue is superseded or no longer relevant.
- **R-working-as-designed** = the issue is valid, but the subcommittee has concluded that the library is working as intended.

### Area

An issue may have one or more *area* labels, indicating subject areas that the issue relates to.  The list of areas may grow over time.  Area labels start with `A-`.

### Optional Labels

The following labels are optional and can be applied to an issue if appropriate:

- **good first issue** = this would be good for a new contributor.
- **v1** = revisit this issue before launching ICU4X v1 stable.
