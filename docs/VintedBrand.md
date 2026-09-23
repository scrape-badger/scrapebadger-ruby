# ScrapeBadger::VintedBrand

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **title** | **String** |  |  |
| **slug** | **String** |  |  |
| **item_count** | **Integer** |  | [optional][default to 0] |
| **favourite_count** | **Integer** |  | [optional][default to 0] |
| **is_luxury** | **Boolean** |  | [optional][default to false] |
| **url** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::VintedBrand.new(
  id: null,
  title: null,
  slug: null,
  item_count: null,
  favourite_count: null,
  is_luxury: null,
  url: null
)
```

