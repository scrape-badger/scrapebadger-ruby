# ScrapeBadger::GitHubPagination

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **has_next** | **Boolean** |  |  |
| **page** | **Integer** |  | [optional] |
| **next_page** | **Integer** |  | [optional] |
| **next_page_token** | **String** |  | [optional] |
| **total** | **Integer** |  | [optional] |
| **page_count** | **Integer** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubPagination.new(
  has_next: null,
  page: null,
  next_page: null,
  next_page_token: null,
  total: null,
  page_count: null
)
```

