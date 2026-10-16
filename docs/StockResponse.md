# ScrapeBadger::StockResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** |  |  |
| **products** | [**Array&lt;StockProduct&gt;**](StockProduct.md) |  |  |
| **missing_product_ids** | **Array&lt;Integer&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::StockResponse.new(
  market: null,
  products: null,
  missing_product_ids: null
)
```

