# ScrapeBadger::VintedPagination

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **current_page** | **Integer** |  |  |
| **total_pages** | **Integer** |  |  |
| **total_entries** | **Integer** |  |  |
| **per_page** | **Integer** |  |  |
| **time** | **Integer** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::VintedPagination.new(
  current_page: null,
  total_pages: null,
  total_entries: null,
  per_page: null,
  time: null
)
```

