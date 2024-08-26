# Strimzi Governance

This document defines project governance for the Strimzi project.

## Project Roles

For governance purposes the project recognises four roles: code owners, maintainers, emeritus code owners, and emeritus maintainers.
At any one time a person may be in 0 or 1 of those roles.

### Component owners

A component owner is responsible for development of a specific subproject or component within Strimzi.
Such components might be represented by a separate GitHub repository within the Strimzi organization (e.g. `strimzi-kafka-bridge`) or by a subdirectory in a GitHub repository (e.g. `./documentation/` in `strimzi-kafka-operator`).
The components owners are identified in the [`COMPONENT-OWNERS`](COMPONENT-OWNERS) file in this repository which also includes the component for which they are responsible.

### Maintainers

A maintainer is actively responsible for the overall development of the whole Strimzi project and all its components.
The maintainers are identified in the [`MAINTAINERS`](MAINTAINERS) file.

Every maintainer is, in effect, also an owner for all components and does not have to be mentioned in the `COMPONENT-OWNERS` file.

### Emeritus code owners and maintainers

An emeritus code owner, or an emeritus maintainer, is someone who is formerly had that role but is no longer actively involved with the project.
Emeritus code owners and Emeritus maintainers are identified in the [`EMERITUS`](EMERITUS) file.

In the rest of this document the term 'maintainer' should be taken to mean 'active maintainer' unless qualified using the term 'emeritus maintainer'.

### Changes in Maintainership

New maintainers are proposed by an existing maintainer and are elected by a vote (see later for the rules of this vote).
If the vote succeeds the proposed maintainer will be invited to become a maintainer.
If the proposed maintainer accepts the invitation:
* Their name will be added to the `MAINTAINERS` file.
* They will be added to the collaborators list of the Strimzi repository with "Write" access
* After 6 months they will be given "Admin" access to the Strimzi repository.

Maintainers can be removed by a vote.
If the vote succeeds:
* Their name will be removed from the `MAINTAINERS` file.
* They will be removed to the collaborators list of the Strimzi repository

Maintainers who wish to become emeritus simply mark the fact by opening a PR against this repository moving their name to the `EMERITUS` file.
The process for reverting from an emeritus maintainer to an active maintainer is the same as for new maintainers.

### Changes in component ownership

New component owners can be proposed by any maintainer and are elected by a vote.
If the vote succeeds the proposed component owner will be invited to become a component owner.
If the proposed component owner accepts the invitation:
* Their name will be added to the `COMPONENT-OWNERS` file.
* Owners of components which have their own GitHub repository will get "Write" rights for given GitHub repository and will be able to merge approved PRs.
* Owners will not get "Admin" rights on any Strimzi GitHub repositories.

Component owners can be removed by a vote.
If the vote succeeds:
* Their name will be removed from the `COMPONENT-OWNERS` file.
* They will be removed to the collaborators list of the Strimzi repository, if any.

Component owners who wish to become emeritus simply mark the fact by opening a PR against this repository moving their name to the `EMERITUS` file.
The process for reverting from an emeritus component owners to an active component owners is the same as for new component owners.

## Voting rules

The Strimzi project employs voting to ensure no single member can dominate the project.

For formal votes, a specific statement of what is being voted on should be added to the relevant GitHub issue or PR.
Voters should indicate their yes/no vote on that issue or PR, and after a suitable period of time, the votes will be tallied and the outcome noted.

The project uses different kinds of vote for different purposes.

* PR approval votes
* Lazy majority votes
* Explicit majority votes

Who may vote, where votes are recorded and the duration of the voting also depends on the subject of vote, as explained in the following sections.

### PR approval rules

PRs against most repositories may be merged after receiving at least two positive maintainer votes.
Voting for PRs can be done using a comment in the PR or by approving (or requesting changes) the PR.
If the PR author is a maintainer, this counts as a vote.

PRs which affect only a single component can be approved by at least one positive maintainer vote and one positive vote from an owner of the given component.
If the PR author is a maintainer or an owner of given component, this counts as a vote.

### Lazy majority rules

Lazy majority votes use +1, 0, -1 votes and their fractions, where:
* +1 means "yes"
* -1 means "no"
* The numbers between +1 and -1 indicate how strongly you feel about the proposal

_(Inspired by [Apache Software Foundation voting](https://www.apache.org/foundation/voting.html#expressing-votes-1-0-1-and-fractions))_

Binding votes are those cast by people in specific roles defined for that vote and count towards the approval of the subject of the vote.
Non-binding may be cast by people not in any of those roles and do not count towards approval of the subject of the vote.

The vote succeeds when there are least three +1 binding votes and no -1 binding votes.
The vote should be opened for at least 3 days to give everyone enough time to vote.

### Explicit majority rules

An explicit majority vote is simply a +1 or -1. 
The vote succeeds when ⅔ of cast binding votes are +1.
The vote should be opened for at least 7 days to give everyone enough time to vote.

### Votes

#### Votes on changes to Governance

With the exception of maintainers and component owners marking themselves as emeritus, all changes in the governance repository require an **Explicit majority** of **Maintainers**.

#### Votes on adding or removing maintainers

Votes to adding or removing a maintainer require an **Explicit majority** of **Maintainers**.

#### Votes on adding or removing component owners

Votes to add or remove a component owners require an **Explicit majority** of **Maintainers**.

#### Votes on Proposals

Proposals can be opened against the [proposals repository](https://github.com/strimzi/proposals).
Proposals should cover any changes to the Strimzi project which might significantly impact its users or the project direction.

Approving a proposal requires a **Lazy majority** of **Maintainers**.
*However, non-binding votes are encouraged as a signal to maintainers of the acceptability of the proposal to the wider community.*

+1 votes can be expressed by approving the proposal PR or in the comments.
Other votes, with reasons, can be expressed in the comments. 
For example "-1 (binding) because ...", or for a non-maintainer "-1 (non-binding) because ...".

#### Votes on PRs in Other Repos

With the exception of the governance and proposals repositories, votes on PRs in other repositories use **PR approval rules**.

#### Votes on Other Changes

Unless specified above, all other changes to the project require an **Explicit majority** of **maintainers**.
Additionally, any maintainer may request that any change require an **Explicit majority** of **maintainers**
