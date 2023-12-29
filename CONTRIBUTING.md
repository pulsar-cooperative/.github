# Pulsar Cooperative - Contributing

First off, thanks for taking the time to contribute! Your effort is greatly appreciated!

This document details the contributing guidelines for all repositories within this organization, and is broken down into two major sections:

* [Contributing Details for End Users](#contributing-details-for-end-users)
* [Contributing Details for Developers](#contributing-details-for-developers)

## Contributing Details for End Users

Welcome to the Pulsar Cooperative! This organization functions a little differently than you might be used to, so it's important to become familiar with how it does, so that you know what to expect when receiving support, or having your issues fixed.

Pulsar Cooperative, is just that, a Cooperative. There is no lead/core/primary developers of this organization or any given repository. Every repository is supported by other developers just like you!

Pulsar Cooperative was born out of a need for Pulsar. With the shutdown of Atom we found many packages started to become archived or abandoned before Pulsar had a chance to alert the maintainers of the new home for their package. This began to result in community packages becoming outdated or broken, with no maintainer available to fix them or accept PRs to fix them. While for some time the messaging from the Pulsar team put the onus of responsibility on the users that reported these errors to republish and support the package with the changes needed to make it work, we slowly realized that not everybody has the time or want to become the steward of these community packages. That even if they may come up with the code fix for the package, they didn't want the ongoing responsibility of it.

From there we realized the necessity of this organization. Where automated process' and some key members can be responsible for publishing new versions of a package, and managing the code and repository, we could then allow the community to step in for the real work. That is reporting and fixing bugs in a package.

Pulsar Cooperative takes all the ongoing support of a package, while community members are then left to their own discretion to report any issues that may occur, as well as fix these reported issues.

What does this mean for you? This means that if you report an error or bug within a package there is no developer assigned to that repository that will come and take a look. Instead we hope that some developer interested in the package will find your issue, and create a fix for it. That way when they offer the fix to the repository a maintainer only has to review these changes and if accepted get them published to the Pulsar Package Registry.

We hope that this system allows developers to do what developers do best, and write good code, while not having to worry about anything else.

So above all what this may mean for you, is to be patient in a solution being offered to your issue. If you worry that you might have to wait to long, the best thing that can be suggested is to find an issue in the repo that you can assist with, if everybody does this, then every issue can be resolved in a timely manner.

## Contributing Details for Developers

It is highly recommended to read through the above section [Contributing Details for End Users](#contributing-details-for-end-users) to ensure developers fully understand the support expected for every repository within this organization.

As for developers that understand the support that should be expected, it's important to remember some key guiding principals when contributing to packages that are available on Pulsar Cooperative:

  * When providing any change to a package, it's important to do everything possible to not alter it's functionality beyond it's original goal. This doesn't mean a new feature can't be added, or a breaking change can't be added, but lets say you contribute to a syntax highlighting package, you shouldn't then add autocomplete, or you shouldn't add linting capabilities. The goal of the package should be kept true, no matter the change being made.
  * It's also important to avoid breaking changes as much as possible. Of course there are times where this is needed, and when that occurs, just ensure it's obvious to those that may read your PR, or that your commit messages detail this.

### Who can Contribute

Anyone! If you have a fondness for a particular package, feel free to turn on notifications and keep an eye on any reported issues, this way you can always try and ensure it functions to it's best ability. Otherwise feel free to browse for any [Good First Issue](https://github.com/pulls?q=is%3Aopen+user%3Apulsar-cooperative+archived%3Afalse+sort%3Acomments-asc+label%3A%22good+first+issue%22) issues listed across the org, to see where you can start helping out for a particular package.

It's important to also mention that contributing doesn't just mean code fixes, triage is very valuable as well, simply detailing where an error occurs in the code, and leaving someone else to think of a solution.

### How to Contribute

To contribute to any package within this org:

1) Find what you'd like to change. This could be a refactor, an update to dependencies, or addressing an issue reported by another user.
2) Then fork the repository to your account to begin your work.
3) While you develop the package and work on bug fixes, please ensure that you use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) in your commit messages. This is how new versions of the package's are released and updated. Failing to follow conventional commits within your PR may mean it will be closed without being merged.
4) Once you have completed your changes, feel free to open up a PR against the repository detailing the changes you've made, and especially if there are any breaking changes, ensure you are justifying and making this obvious.
5) As soon as possible a maintainer of the repository will take the time to review your changes, and communicate any additional changes or modifications that should be made prior to merging.
6) Your PR has been merged! Fantastic! From here a series of automated steps will take place to update the version of the package, according to your helpful Conventional Commits, and this new version will be published to the Pulsar Package Registry, for everyone to use.
