# ScrapeBadger::VintedImageSearchRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **image_url** | **String** |  | [optional] |
| **image_base64** | **String** |  | [optional] |
| **market** | **String** | Vinted market code; uk aliases gb | [optional][default to &#39;fr&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** |  | [optional][default to 20] |
| **price_from** | **Float** |  | [optional] |
| **price_to** | **Float** |  | [optional] |
| **brand_ids** | **String** |  | [optional] |
| **catalog_ids** | **String** |  | [optional] |
| **color_ids** | **String** |  | [optional] |
| **size_ids** | **String** |  | [optional] |
| **material_ids** | **String** |  | [optional] |
| **status_ids** | **String** |  | [optional] |
| **time** | **Integer** |  | [optional] |
| **search_session_id** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::VintedImageSearchRequest.new(
  image_url: null,
  image_base64: null,
  market: null,
  page: null,
  per_page: null,
  price_from: null,
  price_to: null,
  brand_ids: null,
  catalog_ids: null,
  color_ids: null,
  size_ids: null,
  material_ids: null,
  status_ids: null,
  time: null,
  search_session_id: null
)
```

