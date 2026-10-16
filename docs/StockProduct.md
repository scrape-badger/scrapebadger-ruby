# ScrapeBadger::StockProduct

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **Integer** |  |  |
| **product_price** | [**Price**](Price.md) |  | [optional] |
| **is_in_stock** | **Boolean** |  |  |
| **variants** | [**Array&lt;Variant&gt;**](Variant.md) |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::StockProduct.new(
  product_id: null,
  product_price: null,
  is_in_stock: null,
  variants: null
)
```

