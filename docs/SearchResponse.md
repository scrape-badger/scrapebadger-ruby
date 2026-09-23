# ScrapeBadger::SearchResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **items** | [**Array&lt;VintedItemSummary&gt;**](VintedItemSummary.md) |  |  |
| **pagination** | [**VintedPagination**](VintedPagination.md) |  |  |
| **market** | **String** |  |  |
| **seller_country** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::SearchResponse.new(
  items: null,
  pagination: null,
  market: null,
  seller_country: null
)
```

