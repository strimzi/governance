# Releases

This document describes how Strimzi handles versioning, releases new versions and communicates about them.

All Strimzi component releases use [semantic versioning](https://semver.org/).

## Release Cycle

Strimzi uses a 1–2 month release schedule for the "core" operators component.
The [GitHub milestones](https://github.com/strimzi/strimzi-kafka-operator/milestones) are used to track the features and bug fixes included in each release.
There is also a [roadmap](https://github.com/orgs/strimzi/projects/1) to describe the features that will be available in the future releases.

Other Strimzi components don't have a specific release cycle.
New releases are decided on a case-by-case basis depending on the new features added, bugs and vulnerabilities fixed.

## Release Process

Most of the Strimzi components have documentation about how to make a new release.
For example, the release process for the cluster operator is described [here](https://github.com/strimzi/strimzi-kafka-operator/blob/main/development-docs/RELEASE.md).

Before an official release, at least one Release Candidate (RC) is built for testing.
More RCs can follow the first one if new bugs are found along the way.
The Release Candidates are announced on the Slack channel and Strimzi user CNCF mailing list, so that the community can test before the final release.
The maintainers provides 2-3 days to the community for testing and, if no objections are raised, the final release is announced.

## Keeping Track Of Changes

We provide a changelog that includes the main changes for each version taking the history from the first release.
It is available as part of the repository of each component, for example, here is the changelog for the [Strimzi cluster operator](https://github.com/strimzi/strimzi-kafka-operator/blob/main/CHANGELOG.md).

Every closed issue and PR should be added to a GitHub Milestone that provides an overview of everything that will be included in the corresponding release.

Lastly, every new release will come with a GitHub Release which provides the exact changelog for that release.

## Get Notified For New Releases

Every new release, for each component, is announced in several ways:

* Email to the Strimzi users CNCF mailing list.
* Strimzi CNCF Slack channel.

Another way to be notified is by [watching](https://docs.github.com/en/github/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications#configuring-your-watch-settings-for-an-individual-repository) our Strimzi repositories on GitHub, for example the [Strimzi cluster operator](https://github.com/strimzi/strimzi-kafka-operator) one.

## Removing Features, Breaking Changes, Deprecations and Feature Gates

When there is an API deprecation (with or without a replacement) it is announced in the coming release changelog. 
We define a plan about when that API will be completely removed in the future giving the users enough time and the steps needed to adopt the new one.
By API it would mean the Custom Resources schemas and configuration for "core" operators, OpenAPI definition for the HTTP bridge or configuration for the OAuth component.
The notice period between deprecation and removal is defined on a case-by-case basis as part of the proposal or PR that deprecates an API.

New features may be added through [feature gates](https://github.com/strimzi/proposals/blob/main/022-feature-gates.md).
It means that the feature is disabled by default at the beginning but users can start trying it by enabling the corresponding gate.
Even in this case, we describe the plan about when that feature will be enabled by default and removed from the "feature gate".

## Apache Kafka Support

On each new Strimzi cluster operator release, it is not feasible to maintain support for all the available Apache Kafka versions.
There is a well-defined plan for supported Apache Kafka versions you can read [here](https://github.com/strimzi/strimzi-kafka-operator/blob/main/KAFKA_VERSION_SUPPORT.md).