# ScrapeBadger::GitHubActivityBlock

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **summary** | **String** |  |  |
| **count** | **Integer** |  | [optional] |
| **rows** | [**Array&lt;GitHubActivityRow&gt;**](GitHubActivityRow.md) |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubActivityBlock.new(
  type: null,
  summary: null,
  count: null,
  rows: null
)
```

