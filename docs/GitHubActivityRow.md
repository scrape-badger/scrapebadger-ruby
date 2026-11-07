# ScrapeBadger::GitHubActivityRow

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** |  |  |
| **count** | **Integer** |  | [optional] |
| **title** | **String** |  | [optional] |
| **link** | **String** |  | [optional] |
| **repository** | **String** |  | [optional] |
| **repository_link** | **String** |  | [optional] |
| **links** | [**Array&lt;GitHubTextLink&gt;**](GitHubTextLink.md) |  | [optional] |
| **created_at** | **String** |  | [optional] |
| **created_utc** | **Float** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubActivityRow.new(
  text: null,
  count: null,
  title: null,
  link: null,
  repository: null,
  repository_link: null,
  links: null,
  created_at: null,
  created_utc: null
)
```

