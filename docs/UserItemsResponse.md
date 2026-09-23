# ScrapeBadger::UserItemsResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **items** | [**Array&lt;VintedItemSummary&gt;**](VintedItemSummary.md) |  |  |
| **pagination** | [**VintedPagination**](VintedPagination.md) |  |  |
| **market** | **String** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::UserItemsResponse.new(
  items: null,
  pagination: null,
  market: null
)
```

