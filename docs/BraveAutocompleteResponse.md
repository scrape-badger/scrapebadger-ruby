# ScrapeBadger::BraveAutocompleteResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **country** | **String** |  |  |
| **suggestions** | [**Array&lt;BraveSuggestion&gt;**](BraveSuggestion.md) |  |  |
| **result_count** | **Integer** |  |  |
| **source_url** | **String** |  |  |
| **fetched_at** | **String** |  |  |
| **fetched_utc** | **Float** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::BraveAutocompleteResponse.new(
  query: null,
  country: null,
  suggestions: null,
  result_count: null,
  source_url: null,
  fetched_at: null,
  fetched_utc: null
)
```

