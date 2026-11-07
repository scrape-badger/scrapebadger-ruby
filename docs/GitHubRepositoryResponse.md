# ScrapeBadger::GitHubRepositoryResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **repository** | [**GitHubRepositoryIdentity**](GitHubRepositoryIdentity.md) |  |  |
| **latest_commit** | [**GitHubLatestCommit**](GitHubLatestCommit.md) |  | [optional] |
| **readme** | [**GitHubRepositoryReadme**](GitHubRepositoryReadme.md) |  | [optional] |
| **files** | [**Array&lt;GitHubRepositoryFile&gt;**](GitHubRepositoryFile.md) |  | [optional] |
| **languages** | [**Array&lt;GitHubRepositoryLanguage&gt;**](GitHubRepositoryLanguage.md) |  | [optional] |
| **latest_release** | [**GitHubRepositoryRelease**](GitHubRepositoryRelease.md) |  | [optional] |
| **contributors** | [**Array&lt;GitHubRepositoryAccount&gt;**](GitHubRepositoryAccount.md) |  | [optional] |
| **contributors_truncated** | **Boolean** |  | [optional] |
| **dependents** | [**Array&lt;GitHubRepositoryAccount&gt;**](GitHubRepositoryAccount.md) |  | [optional] |
| **dependents_truncated** | **Boolean** |  | [optional] |
| **funding** | [**GitHubRepositoryFunding**](GitHubRepositoryFunding.md) |  | [optional] |
| **community_files** | [**Array&lt;GitHubCommunityFile&gt;**](GitHubCommunityFile.md) |  | [optional] |
| **metadata_available** | **Boolean** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubRepositoryResponse.new(
  repository: null,
  latest_commit: null,
  readme: null,
  files: null,
  languages: null,
  latest_release: null,
  contributors: null,
  contributors_truncated: null,
  dependents: null,
  dependents_truncated: null,
  funding: null,
  community_files: null,
  metadata_available: null
)
```

