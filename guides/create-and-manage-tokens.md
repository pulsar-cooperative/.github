# Create and Manage Tokens for the Organization

Within this organization there are two tokens that are very important for use within every repository, and their actions.

Each token must be made with an account that has admin access to the org, and it's recommended to create these as Fine-grained access tokens.

## PPR_TOKEN

- Access on the pulsar-cooperative organization
- Repository Access: All repositories
- Repository Permissions:
  * Contents: `read-only`
  * Metadata: `read-only`

This token value is then set as an organization secret for `pulsar-cooperative` as: `PPR_AUTH`.

### GITHUB_REPO_TOKEN

- Access on the pulsar-cooperative organization
- Repository Access: All repositories
- Repository Permissions:
  * Contents: `read-and-write`
  * Metadata: `read-only`
  * Pull Requests: `read-and-write`
  * Variables: `read-and-write`

This token value is then set as an organization secret for `pulsar-cooperative` as: `REPO_TOKEN`.
