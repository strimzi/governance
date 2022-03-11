# Releases

This document describes how Strimzi handles versioning, releases new versions and communicates about them.

Strimzi uses [semantic versioning](https://semver.org/) as a versioning schema for the releases of all the components.

## Release Cycle

Strimzi is using a release schedule of 1 or 2 months for the "core" component, the cluster operator.
The [GitHub milestones](https://github.com/strimzi/strimzi-kafka-operator/milestones) are used to track the features and bug fixes included in each release.

The other components, under the Strimzi umbrella, don't have a specific release cycle but when having a new releases is decided on a case-by-case basis depending on the new features added, bugs and vulnerabilities fixed.

## Release Process

Most of the Strimzi components have a corresponding documentation about how to make a new release.
For example, the release process for the cluster operator is described [here](https://github.com/strimzi/strimzi-kafka-operator/blob/main/development-docs/RELEASE.md).

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

When there is an API deprecation, because it is going to be replaced by a new one, it is announced in the coming release changelog. 
We define a plan about when that API will be completely removed in the future giving the users enough time and the steps needed to adopt the new one.

New features could be added through the so called "feature gates".
It means that the feature is disabled by default at the beginning but users can start trying it by enabling the corresponding gate.
Even in this case, we describe the plan about when that feature will be enabled by default and removed from the "feature gate".

## Apache Kafka Support

On each new Strimzi cluster operator release, it is not feasible to maintain support for all the available Apache Kafka versions.
There is a well defined plan for supported Apache Kafka versions you can read [here](https://github.com/strimzi/strimzi-kafka-operator/blob/main/KAFKA_VERSION_SUPPORT.md).