# ScrapeBadger::VintedItemSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **title** | **String** |  |  |
| **price** | [**VintedPrice**](VintedPrice.md) |  |  |
| **brand_title** | **String** |  | [optional] |
| **display_title** | **String** |  | [optional] |
| **display_subtitle** | **String** |  | [optional] |
| **size_title** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **url** | **String** |  |  |
| **path** | **String** |  | [optional] |
| **is_visible** | **Boolean** |  | [optional][default to true] |
| **promoted** | **Boolean** |  | [optional][default to false] |
| **favourite_count** | **Integer** |  | [optional][default to 0] |
| **view_count** | **Integer** |  | [optional][default to 0] |
| **service_fee** | **String** |  | [optional] |
| **total_item_price** | **String** |  | [optional] |
| **content_source** | **String** |  | [optional] |
| **seller_country_code** | **String** |  | [optional] |
| **similarity_score** | **Float** |  | [optional] |
| **user** | [**VintedUserSummary**](VintedUserSummary.md) |  | [optional] |
| **photo** | [**VintedPhoto**](VintedPhoto.md) |  | [optional] |
| **photos** | [**Array&lt;VintedPhoto&gt;**](VintedPhoto.md) |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::VintedItemSummary.new(
  id: null,
  title: null,
  price: null,
  brand_title: null,
  display_title: null,
  display_subtitle: null,
  size_title: null,
  status: null,
  url: null,
  path: null,
  is_visible: null,
  promoted: null,
  favourite_count: null,
  view_count: null,
  service_fee: null,
  total_item_price: null,
  content_source: null,
  seller_country_code: null,
  similarity_score: null,
  user: null,
  photo: null,
  photos: null
)
```

