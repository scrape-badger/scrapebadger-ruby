# ScrapeBadger::AutoScout24ListingResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** |  |  |
| **source_url** | **String** |  |  |
| **listing** | [**AutoScout24ListingDetail**](AutoScout24ListingDetail.md) |  |  |
| **latency_ms** | **Integer** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::AutoScout24ListingResponse.new(
  market: null,
  source_url: null,
  listing: null,
  latency_ms: null
)
```

