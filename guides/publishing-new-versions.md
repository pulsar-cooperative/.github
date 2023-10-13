# Publishing New Versions

The process of publishing a new package version is one that tries to find the middle ground between a hands on approach and automation, tending to not lean too heavily into automation.

The general workflow of publishing a new version looks like this.

Keeping in mind that it's assumed at this point that the initial new package has already been published, and the GitHub Secret `PUBLISHED` has been set to `true` (**Match the case!**).

1. A contributor creates a new PR to the repository. It has been successfully reviewed, and is ready to merge.
2. The PR is merged, causing the workflow `version-bump.yml` to trigger, and use Google's [release-please](https://github.com/googleapis/release-please) to draft a new version bump (according to [Conventional Commit](https://www.conventionalcommits.org/) conventions) and an associated new tag.
3. Once this PR is then merged, you are ready to publish a new version!
4. Manually run the workflow `release.yml` to trigger the publication of a new package version to PPR.
5. You're done! As you can see the total process to publish a new version, including the initial contributors PR boils down to:

* Merge 2 PRs (the original contributors, and the one created by `release-please`)
* Manually trigger 1 workflow, to publish the package.
