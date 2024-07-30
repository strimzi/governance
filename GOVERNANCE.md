# Strimzi Governance

This document defines project governance for the Strimzi project.

## Project Roles

### Maintainers

The maintainers are responsible for the overall development of the whole Strimzi project and all its components.
Emeritus maintainers are former maintainers who are no longer actively involved in the project.
In the rest of this document the term ‘maintainer’ will be assumed to mean ‘active maintainer’, unless qualified as ‘emeritus maintainer’.
Both maintainers and emeritus maintainers are identified in the [`MAINTAINERS`](MAINTAINERS) file. 

#### Changes in Maintainership

New maintainers are proposed by an existing maintainer and are elected by a ⅔ majority maintainers vote.
Maintainers can be removed by a ⅔ majority maintainers vote. 
Maintainers removed by a vote are no longer considered maintainers or emeritus maintainers.
Maintainers become emeritus maintainers either actively, by opening a PR against the MAINTAINERS file marking themselves as Emeritus, or implicitly after 6 months without any contribution to the project.

### Emeritus maintainers

An Emeritus maintainer has still access to all the Strimzi venues (e.g. Slack, Email, Community call, etc.).
They can contribute to the project in any way which doesn't implies strong and long term commitment, as active maintainers do.
The MAINTAINERS file may not always immediately reflect implicit emeritus status, as updates to mark maintainers as Emeritus are done asynchronously.
An Emeritus maintainer reverts to being an active maintainer by starting a voting process.
The voting process can also be started by an active maintainer instead.
At least three +1 binding votes and no -1 binding votes, from active maintainers, are needed to accept the emeritus one to be considered active again.

#### Github Project Administration

Maintainers will be added to the collaborators list of the Strimzi repository with "Write" access.
After 6 months a maintainer will be given "Admin" access to the Strimzi repository.

### Component owners

The component owners are responsible for development of a specific subproject or component within Strimzi.
Such components might be represented by a separate GitHub repository within the Strimzi organization (e.g. `strimzi-kafka-bridge`) or by a subdirectory in a GitHub repository (e.g. `./documentation/` in `strimzi-kafka-operator`).
The components owners are identified in the [`COMPONENT-OWNERS`](COMPONENT-OWNERS) file in this repository which also includes the component for which they are responsible.

By definition, every maintainer is also an owner for all components and does not have to be mentioned in the `OWNERS` list.

#### Changes in component ownership

New component owners can be proposed by any maintainer and are elected by a ⅔ majority maintainers vote.
Component owners can be removed by a ⅔ majority maintainers vote.

#### Github Project Administration

Owners of components which have their own GitHub repository will get "Write" rights for that GitHub repository and will be able to merge approved PRs.
Owners will not get "Admin" rights on any Strimzi GitHub repositories.

## Voting

The Strimzi project employs voting to ensure no single member can dominate the project.

For formal votes, a specific statement of what is being voted on should be added to the relevant GitHub issue or PR.
Voters should indicate their yes/no vote on that issue or PR, and after a suitable period of time, the votes will be tallied and the outcome noted.

### Approving PRs

PRs may be merged after receiving at least two positive maintainer votes.
Voting for PRs can be done using a comment in the PR or by approving (or requesting changes) the PR.
If the PR author is a maintainer, this counts as a vote.

PRs which affect only a single component can be approved by at least one positive maintainer vote and one positive vote from an owner of that component.
If the PR author is a maintainer or an owner of that component, this counts as a vote.

### Proposals

Proposals can be opened against the [proposals repository](https://github.com/strimzi/proposals).
Proposals should cover any changes to the Strimzi project which might significantly impact its users or the project direction.

Voting about proposals is using +1, 0, -1 votes and their fractions, where:
* +1 means "yes"
* -1 means "no"
* The numbers between +1 and -1 indicate how strongly you feel about the proposal

_(Inspired by [Apache Software Foundation voting](https://www.apache.org/foundation/voting.html#expressing-votes-1-0-1-and-fractions))_

Votes from maintainers are binding and count towards the approval of the proposal.
Non-maintainers are allowed and encouraged to vote as well.
But their votes are non-binding and do not count towards approval of the proposal.

+1 votes can be expressed by approving the proposal PR or in the comments.
Other votes should be expressed in the comments.
For example "+1 (binding)", or for a non-maintainer "+1 (non-binding)".

Proposals are approved when they receive at least three +1 binding votes and no -1 binding votes.
The proposal PR should be opened for at least 3 days to give everyone enough time to vote.

### Changes in Governance

All changes in Governance require a ⅔ majority maintainers vote.

### Other Changes

Unless specified above, all other changes to the project require a ⅔ majority maintainers vote.
Additionally, any maintainer may request that any change require a ⅔ majority maintainers vote.
