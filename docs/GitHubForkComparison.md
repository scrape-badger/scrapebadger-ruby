# ScrapeBadger::GitHubForkComparison

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ahead** | **Integer** |  |  |
| **behind** | **Integer** |  |  |
| **base_branch** | **String** |  |  |
| **current_ref** | **String** |  |  |
| **is_tracking_branch** | **Boolean** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubForkComparison.new(
  ahead: null,
  behind: null,
  base_branch: null,
  current_ref: null,
  is_tracking_branch: null
)
```

