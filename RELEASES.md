# Releases

This document describes how Strimzi handles versioning, releases new versions and communicates about them.

Strimzi uses [semantic versioning](https://semver.org/) as a versioning schema for the releases of all the components.

## Release Cycle

Strimzi is using a release schedule of 1/2 months for the "core" component, the cluster operator.
The [GitHub milestones](https://github.com/strimzi/strimzi-kafka-operator/milestones) are used to track the features and bug fixes included in each release.

The other components, under the Strimzi umbrella, don't have a specific release cycle but when having a new releases is decided on a case-by-case basis depending on the new features added, bugs and vulnerabilities fixed.

## Release Process

Every Strimzi component has a corresponding documentation about how to make a new release.
For example, the release process for the cluster operator is described [here](https://github.com/strimzi/strimzi-kafka-operator/blob/main/development-docs/RELEASE.md).

## Keeping Track Of Changes

We provide a changelog that includes all changes for each version taking the history from the first release.
It is available as part of the repository of each component, for example, here is the changelog for the [Strimzi cluster operator](https://github.com/strimzi/strimzi-kafka-operator/blob/main/CHANGELOG.md).

Every closed issue and PR should be added to a GitHub Milestone that provides an overview of everything that will be included in the corresponding release.

Lastly, every new release will come with a GitHub Release which provides the exact changelog for that release.

## Get Notified For New Releases

Every new release, for each component, is announced in several ways:

* Email to the Strimzi users CNCF mailing list.
* Strimzi CNCF Slack channel.
* Twitter [account](https://twitter.com/strimziio).

Another way to be notified is by [watching](https://docs.github.com/en/github/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications#configuring-your-watch-settings-for-an-individual-repository) our Strimzi repositories on GitHub, for example the [Strimzi cluster operator](https://github.com/strimzi/strimzi-kafka-operator) one.

## Removing Features, Breaking Changes, Deprecations and Feature Gates

Every new major version, Strimzi maintainers are allowed to remove features or make breaking changes as per [semantic versioning](https://semver.org/).

When there is an API deprecation, because it is going to be replaced by a new one, it is announced in the coming release changelog. 
We define a plan about when that API will be completely removed in the future giving the users enough time and the steps needed to adopt the new one.

New features could be added through the so called "feature gates".
It means that the feature is disabled by default but users can start trying it by enabling the corresponding gate.
Even in this case, we describe the plan about when that feature will be enabled by default and removed from the "feature gate".