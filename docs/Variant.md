# ScrapeBadger::Variant

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **variant_id** | **Integer** |  | [optional] |
| **id** | **Integer** |  | [optional] |
| **size** | **String** |  | [optional] |
| **brand_size** | **String** |  | [optional] |
| **size_id** | **Integer** |  | [optional] |
| **colour** | **String** |  | [optional] |
| **colour_way_id** | **Integer** |  | [optional] |
| **sku** | **String** |  | [optional] |
| **is_available** | **Boolean** |  | [optional] |
| **is_in_stock** | **Boolean** |  | [optional] |
| **is_low_in_stock** | **Boolean** |  | [optional] |
| **is_restocking_soon** | **Boolean** |  | [optional] |
| **price** | [**Price**](Price.md) |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::Variant.new(
  variant_id: null,
  id: null,
  size: null,
  brand_size: null,
  size_id: null,
  colour: null,
  colour_way_id: null,
  sku: null,
  is_available: null,
  is_in_stock: null,
  is_low_in_stock: null,
  is_restocking_soon: null,
  price: null
)
```

