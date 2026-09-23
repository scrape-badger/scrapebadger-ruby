# ScrapeBadger::VintedItemDetail

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
| **description** | **String** |  | [optional] |
| **catalog_id** | **Integer** |  | [optional] |
| **color1** | **String** |  | [optional] |
| **color2** | **String** |  | [optional] |
| **package_size_id** | **Integer** |  | [optional] |
| **is_favourite** | **Boolean** |  | [optional][default to false] |
| **can_buy** | **Boolean** |  | [optional][default to true] |
| **can_bundle** | **Boolean** |  | [optional][default to false] |
| **can_reserve** | **Boolean** |  | [optional][default to false] |
| **instant_buy** | **Boolean** |  | [optional][default to false] |
| **is_hidden** | **Boolean** |  | [optional][default to false] |
| **is_reserved** | **Boolean** |  | [optional][default to false] |
| **is_closed** | **Boolean** |  | [optional][default to false] |
| **seller** | [**VintedSellerSummary**](VintedSellerSummary.md) |  | [optional] |
| **size_id** | **Integer** |  | [optional] |
| **status_id** | **Integer** |  | [optional] |
| **brand_id** | **Integer** |  | [optional] |
| **category** | **Array&lt;String&gt;** |  | [optional] |
| **upload_date** | **String** |  | [optional] |
| **uploaded_at** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::VintedItemDetail.new(
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
  photos: null,
  description: null,
  catalog_id: null,
  color1: null,
  color2: null,
  package_size_id: null,
  is_favourite: null,
  can_buy: null,
  can_bundle: null,
  can_reserve: null,
  instant_buy: null,
  is_hidden: null,
  is_reserved: null,
  is_closed: null,
  seller: null,
  size_id: null,
  status_id: null,
  brand_id: null,
  category: null,
  upload_date: null,
  uploaded_at: null
)
```

