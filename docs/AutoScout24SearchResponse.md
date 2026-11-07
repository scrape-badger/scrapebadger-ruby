# ScrapeBadger::AutoScout24SearchResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** |  |  |
| **source_url** | **String** |  |  |
| **total_results** | **Integer** |  |  |
| **total_pages** | **Integer** |  |  |
| **page** | **Integer** |  |  |
| **page_size** | **Integer** |  | [optional][default to 20] |
| **has_next_page** | **Boolean** |  |  |
| **next_page** | **Integer** |  |  |
| **pagination_cap** | **Integer** |  | [optional][default to 200] |
| **results** | [**Array&lt;AutoScout24Listing&gt;**](AutoScout24Listing.md) |  |  |
| **filters** | **Hash&lt;String, Object&gt;** |  |  |
| **applied_filters** | **Hash&lt;String, Object&gt;** |  |  |
| **latency_ms** | **Integer** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::AutoScout24SearchResponse.new(
  market: null,
  source_url: null,
  total_results: null,
  total_pages: null,
  page: null,
  page_size: null,
  has_next_page: null,
  next_page: null,
  pagination_cap: null,
  results: null,
  filters: null,
  applied_filters: null,
  latency_ms: null
)
```

