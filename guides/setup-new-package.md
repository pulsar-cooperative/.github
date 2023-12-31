# Setup a New Package for Pulsar Cooperative

This guide will walk you through the steps needed to configure and setup a brand new forked package on Pulsar Cooperative.

## Renaming the Package/Repository

Since the original name of the package is reserved on the Pulsar Package Registry, it will need to be renamed, both within the `package.json` as well as the repository name itself (while the name doesn't have to change, it's best practice to keep these names in sync).

When renaming the package the loose convention would be to reuse the original package name, but adding `-pulsar` to the end, such as `[original-name]-pulsar` e.g. `language-cobol-pulsar`. Alternatively, many packages have `atom` in the name of the package, this could also be changed to just `pulsar`, such as `atom-ternjs` => `pulsar-ternjs`.

## Configuring the Repository

This repository has several helpful template resources to aide in the initial setup, these resources are available within `./package-template` and show the text that should be added to a package's readme, as well as many of the actions that will be needed.

You'll also want to ensure that `Issues` are enabled for this new repository.

### Configuring Repository Settings

This setup relates to settings that must be changed on the repository itself, via the GitHub website.

* Add the following values to the repository's secrets/variables:

  - `PPR_AUTH`: This should be set at the organization level, and does not need to be set per repository. This should be a Pulsar Package Registry API key, that allows access to the PPR under this organizations name.
  - `PUBLISHED`: This is a value that represents a boolean (although it's still just text) that determines if the package has been published to the PPR already. Using this allows us to ensure that automatic version updates aren't done prior to the package being ready, and ensures we don't accidentally try to publish it twice. This value should not be set manually prior to the package being published, as its lack of existence works just as well as creating it manually and setting it to `false`. Otherwise the `publish.yml` GitHub workflow will create this variable as `true` once run.
  - `REPO_NAME`: This value **must** be created manually, and should be the repository's name, which should match the name used on the Pulsar Package Registry.
  - `REPO_TOKEN`: This should be set at the organization level, and does not need to be set per repository. This should be a GitHub access token with `repo` scope, so that it can modify repository variables as needed.

* You'll then want to ensure to add `pulsar-package` to the package's "topic's" on the GitHub UI to help make this package more discoverable.

### Configuring Repository Files

From here, you'll want to match the template files as closely as possible. You will need to copy the workflows and add the text from the readme template to the package readme.

An important note about these workflow files: the template contains a `test.yml` that is used to run automatic tests on the package during every single PR. The package being forked may already have workflow files to do this, so you'll need to investigate every single workflow file already present to determine if they need to be kept, or modified, to work on this new org. Some packages may use a different testing scheme, which means we can't use the template one, so make sure to take a close look. It may be wise to look at any other workflow files, if they are present, to make sure everything is accounted for.

## Publish this New Package

Once all changes are merged into the package's repository, ensure to manually run the `publish.yaml` or `Publish Package for the First Time` workflow.

## Broadcasting this New Package

Now that the repository is fully setup, and ready for the community to contribute, we need to ensure the community is aware of this new package. The best way to do so is by adding a `badge` to the original package, that recommends installation of this new one.

To get the badge added to the original package, it's best to create a new issue on the [`pulsar-edit/package-backend`](https://github.com/pulsar-edit/package-backend) repository, asking for the new badge to be created. This issue will need to detail the original package name, and the new package name, with links to both.
