# Forking a New Package

This documentation details the criteria that should be used for determining if an existing package should be forked into the `pulsar-cooperative` organization.

While making these choices, be very mindful of the reason this org exists:
This org is intended to allow a package to continue it's useful lifespan after such a time that it would be impossible to do so otherwise. To make sure users and contributors have a place to report issues with a package where they will be heard, and have a place to make contributions to a package where they will be reviewed.

Bearing this in mind, below are the loose guidelines that should be followed and considered when forking a community package:

* Is this package archived? An archived package means that no new issues or PRs can be created, and this new repo may be the only place for the community to be heard.
* Is this package abandoned? While difficult to determine, make sure to keep in mind more than the last commit date. Are there issues left unaddressed? PR's that have never been reviewed or commented on? How long has it been since this repo was ever interacted with by anyone with write access?
* Is the community requesting this package? Make sure that if so, these same community members have already made a best effort to get improvements onto the main package, and that they have not been heard there. This doesn't just mean that an issue hasn't been responded to for a couple days, but an unattended to PR is a good indication that the community does want to help keep the package alive.
* Does this package need further improvements or updates, including security-related ones? Is the package complex enough to warrant keeping it's codebase and taking the time to fork it over?

Lastly some points of knowledge that should be considered:

* Packages from the original `atom` organization, or in some cases labeled as `atom-archived` generally would get an immediate greenlight to fork. Although it should first be checked if these packages already exist on the `pulsar-edit` repo, considering if they have been archived there.
* Packages from the `AtomLinter` organization are generally an immediate greenlight to fork.
* Packages from the `Atom-Community` organization are generally an immediate greenlight to fork.
