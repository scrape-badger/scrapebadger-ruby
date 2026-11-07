# ScrapeBadger::GitHubRepositoryFile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **path** | **String** |  |  |
| **type** | **String** |  |  |
| **link** | **String** |  |  |
| **has_simplified_path** | **Boolean** |  | [optional] |
| **latest_commit** | [**GitHubLatestCommit**](GitHubLatestCommit.md) |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubRepositoryFile.new(
  name: null,
  path: null,
  type: null,
  link: null,
  has_simplified_path: null,
  latest_commit: null
)
```

