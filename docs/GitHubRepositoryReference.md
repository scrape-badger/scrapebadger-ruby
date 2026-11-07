# ScrapeBadger::GitHubRepositoryReference

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **full_name** | **String** |  |  |
| **link** | **String** |  |  |
| **id** | **Integer** |  | [optional] |
| **owner** | [**GitHubRepositoryAccount**](GitHubRepositoryAccount.md) |  | [optional] |
| **description** | **String** |  | [optional] |
| **default_branch** | **String** |  | [optional] |
| **language** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubRepositoryReference.new(
  name: null,
  full_name: null,
  link: null,
  id: null,
  owner: null,
  description: null,
  default_branch: null,
  language: null
)
```

