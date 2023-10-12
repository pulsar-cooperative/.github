# Setup a New Package for Pulsar Cooperative

This guide will walk you through the steps needed to configure and setup a brand new forked package on Pulsar Cooperative.

## Configuring the Repository

This repository has several helpful template resources to aide in the initial setup, these resources are available within `./package-template` and show the text that should be added to a package's readme, as well as many of the actions that will be needed.

### Configuring Repository Settings

This setup relates to settings that must be changed on the repository itself, via the GitHub website.

* Add the following values to the repositories secrets:

  - `PPR_AUTH`: This should be a Pulsar Package Registry API key, that allows access to the PPR under this organizations name.
  - `PUBLISHED`: This is a value that represents a boolean (Although it's still just text) that determines if the package has been published to the PPR already. Using this allows us to ensure that automatic version updates aren't done prior to the package being ready, and ensures we don't accidentally try to publish it twice. Prior to the package being published ensure to set it to `false` and once it's been published for the first time set it to `true` (Match the case!).

* You'll then want to ensure to add `pulsar-package` to the package's 'topic's on the GitHub UI to help make this package more discoverable.

### Configuring Repository Files

From here, you'll want to match the template files as closely as possible.

Copying over the workflows, and adding the text from the readme.

And important note about these workflow files, is the template contains a `test.yml`, this is used to run automatic tests on the package during every single PR. The package being forked may already have workflow files to do this. So you'll need to investigate every single workflow file already present to determine if they need to be kept, or modified to work on this new org. Some packages may use a different testing schema, that means we can't use the template one, so make sure to take a close look!
