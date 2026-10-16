# ScrapeBadger::ProductPrice

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **current** | [**PriceValue**](PriceValue.md) |  | [optional] |
| **previous** | [**PriceValue**](PriceValue.md) |  | [optional] |
| **rrp** | [**PriceValue**](PriceValue.md) |  | [optional] |
| **currency** | **String** |  | [optional] |
| **is_marked_down** | **Boolean** |  | [optional][default to false] |
| **is_outlet_price** | **Boolean** |  | [optional][default to false] |
| **discount_percentage** | **Float** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::ProductPrice.new(
  current: null,
  previous: null,
  rrp: null,
  currency: null,
  is_marked_down: null,
  is_outlet_price: null,
  discount_percentage: null
)
```

