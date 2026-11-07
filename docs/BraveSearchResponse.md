# ScrapeBadger::BraveSearchResponse

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
| **page** | **Integer** |  |  |
| **has_next** | **Boolean** |  |  |
| **next_page** | [**NextPage**](NextPage.md) |  | [optional] |
| **faq** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |
| **discussions** | [**Array&lt;BraveResult&gt;**](BraveResult.md) |  | [optional] |
| **videos** | [**Array&lt;BraveResult&gt;**](BraveResult.md) |  | [optional] |
| **news** | [**Array&lt;BraveResult&gt;**](BraveResult.md) |  | [optional] |
| **images** | [**Array&lt;BraveResult&gt;**](BraveResult.md) |  | [optional] |
| **related_searches** | **Array&lt;Hash&lt;String, String&gt;&gt;** |  | [optional] |
| **rich_blocks** | **Hash&lt;String, Object&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::BraveSearchResponse.new(
  query: null,
  country: null,
  ui_language: null,
  safe_search: null,
  result_count: null,
  results: null,
  query_info: null,
  source_url: null,
  fetched_at: null,
  fetched_utc: null,
  page: null,
  has_next: null,
  next_page: null,
  faq: null,
  discussions: null,
  videos: null,
  news: null,
  images: null,
  related_searches: null,
  rich_blocks: null
)
```

