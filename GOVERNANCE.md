# Strimzi Governance

This document defines project governance for the Strimzi project.

## Project Roles

### Maintainers

The maintainers are responsible for the overall development of the whole Strimzi project and all its components.
The maintainers are identified in the [`MAINTAINERS`](MAINTAINERS) file. 

#### Changes in Maintainership

New maintainers are proposed by an existing maintainer and are elected by a ⅔ majority maintainers vote.
Maintainers can be removed by a ⅔ majority maintainers vote.

#### Github Project Administration

Maintainers will be added to the collaborators list of the Strimzi repository with "Write" access.
After 6 months a maintainer will be given "Admin" access to the Strimzi repository.

### Component owners

The component owners are responsible for development of a specific subproject or components within Strimzi.
Such components might be represented by by a separate GitHub repository within the Strimzi organization (e.g. `strimzi-kafka-bridge`) or by a subdirectory in a GitHub repository (e.g. `./documentation/` in `strimzi-kafka-operator`).
The components owners are identified in the [`COMPOENENT-OWNERS`](COMPONENT-OWNERS) file in this repository which also includes the component for which they are responsible.
Additionally, each of the components will have `OWNERS` file in its root listing the owners.

By definition, every maintainer is also owner for all components and does not have to be mentioned in the `OWNERS` list.

#### Changes in component ownership

New component owners can be proposed by any maintainer and are elected by a ⅔ majority maintainers vote.
Component owners can be removed by a ⅔ majority maintainers vote.

#### Github Project Administration

Owners of components which have their own GitHub repository will get commit rights for given GitHub repository.

## Voting

The Strimzi project employs voting to ensure no single member can dominate the project.

For formal votes, a specific statement of what is being voted on should be added to the relevant GitHub issue or PR.
Voters should indicate their yes/no vote on that issue or PR, and after a suitable period of time, the votes will be tallied and the outcome noted.

### Approving PRs

PRs may be merged after receiving at least two positive maintainer votes.
Voting for PRs can be done using a comment in the PR or by approving (or requesting changes) the PR.
If the PR author is a maintainer, this counts as a vote.

PRs which affect only a single component can be approved by at least one positive maintainer vote and one positive vote from an owner of given component.
If the PR author is a maintainer or an owner of given component, this counts as a vote.

### Proposals

Proposals can be opened against the [proposals repository](https://github.com/strimzi/proposals).
Proposals should cover any changes to the Strimzi project which might significantly impact its users or the project direction.
Proposals are approved by a ⅔ majority maintainers vote.

### Changes in Governance

All changes in Governance require a ⅔ majority maintainers vote.

### Other Changes

Unless specified above, all other changes to the project require a ⅔ majority maintainers vote.
Additionally, any maintainer may request that any change require a ⅔ majority maintainers vote.

