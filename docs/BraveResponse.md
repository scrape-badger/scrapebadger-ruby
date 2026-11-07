# ScrapeBadger::BraveResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **country** | **String** |  |  |
| **ui_language** | **String** |  |  |
| **safe_search** | **String** |  |  |
| **result_count** | **Integer** |  |  |
| **results** | [**Array&lt;BraveResult&gt;**](BraveResult.md) |  |  |
| **query_info** | **Hash&lt;String, Object&gt;** |  |  |
| **source_url** | **String** |  |  |
| **fetched_at** | **String** |  |  |
| **fetched_utc** | **Float** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::BraveResponse.new(
  query: null,
  country: null,
  ui_language: null,
  safe_search: null,
  result_count: null,
  results: null,
  query_info: null,
  source_url: null,
  fetched_at: null,
  fetched_utc: null
)
```

