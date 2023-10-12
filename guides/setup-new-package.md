# Setup a New Package for Pulsar Cooperative

This guide will walk you through the steps needed to configure and setup a brand new forked package on Pulsar Cooperative.

## Configuring the Repository

This repository has several helpful template resources to aide in the initial setup, these resources are available within `./package-template` and show the text that should be added to a package's readme, as well as many of the actions that will be needed.

### Configuring Repository Settings

This setup relates to settings that must be changed on the repository itself, via the GitHub website.

* Add the following values to the repositories secrets/variables:

  - `PPR_AUTH`: This should be set at the organization level, and does not need to be set per repository. But this should be a Pulsar Package Registry API key, that allows access to the PPR under this organizations name.
  - `PUBLISHED`: This is a value that represents a boolean (Although it's still just text) that determines if the package has been published to the PPR already. Using this allows us to ensure that automatic version updates arne't done prior to the package being ready, and ensures we don't accidentally try to publish it twice. Prior to the package being published. Don't set this value manually, as it's lack of existance works just as well as creating it manually and setting it to `false`. Otherwise the `publish.yml` GitHub workflow will create this variable as `true` once run.
  - `REPO_NAME`: This value **must** be created manually, and should be the repositories name, which should match the name used on the Pulsar Package Registry.
  - `GITHUB_REPO_TOKEN`: This should be set at the organization level, and does not need to be set per repository. But this should be a GitHub access token with `repo` scope, so that it can modify repository variables as needed.

* You'll then want to ensure to add `pulsar-package` to the package's 'topic's on the GitHub UI to help make this package more discoverable.

### Configuring Repository Files

From here, you'll want to match the template files as closely as possible.

Copying over the workflows, and adding the text from the readme.

And important note about these workflow files: the template contains a `test.yml` that is used to run automatic tests on the package during every single PR. The package being forked may already have workflow files to do this, so you'll need to investigate every single workflow file already present to determine if they need to be kept, or modified to work on this new org. Some packages may use a different testing scheme, which means we can't use the template one, so make sure to take a close look. It may be wise to look at any other workflow files, if they are present, to make sure everything is accounted for.
