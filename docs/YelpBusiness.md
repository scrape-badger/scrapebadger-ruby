# ScrapeBadger::YelpBusiness

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **position** | **Integer** | 1-based place in Yelp&#39;s organic order across pages (page 2 starts at 11): Yelp&#39;s own number where it numbers the results; services searches are unnumbered and keep Yelp&#39;s order. For ads, the slot order. |  |
| **is_ad** | **Boolean** |  |  |
| **id** | **String** | Yelp encrypted business ID. |  |
| **_alias** | **String** | Business slug used in /biz/&lt;alias&gt;. |  |
| **name** | **String** |  |  |
| **url** | **String** |  |  |
| **rating** | **Float** |  | [optional] |
| **review_count** | **Integer** |  | [optional] |
| **price** | **String** |  | [optional] |
| **price_level** | **Integer** |  | [optional] |
| **categories** | [**Array&lt;YelpCategory&gt;**](YelpCategory.md) |  | [optional] |
| **neighborhoods** | **Array&lt;String&gt;** |  | [optional] |
| **address** | **String** |  | [optional] |
| **city** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **timezone** | **String** |  | [optional] |
| **opening_hours** | [**Array&lt;YelpHours&gt;**](YelpHours.md) |  | [optional] |
| **snippet** | **String** |  | [optional] |
| **snippet_type** | **String** |  | [optional] |
| **highlights** | **Array&lt;String&gt;** |  | [optional] |
| **tags** | **Array&lt;String&gt;** |  | [optional] |
| **photos** | **Array&lt;String&gt;** |  | [optional] |
| **alternate_names** | **Array&lt;String&gt;** |  | [optional] |
| **is_service_area_business** | **Boolean** |  | [optional] |
| **is_yelp_guaranteed** | **Boolean** |  | [optional] |
| **has_verified_license** | **Boolean** |  | [optional] |
| **ad_placement** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::YelpBusiness.new(
  position: null,
  is_ad: null,
  id: null,
  _alias: null,
  name: null,
  url: null,
  rating: null,
  review_count: null,
  price: null,
  price_level: null,
  categories: null,
  neighborhoods: null,
  address: null,
  city: null,
  phone: null,
  timezone: null,
  opening_hours: null,
  snippet: null,
  snippet_type: null,
  highlights: null,
  tags: null,
  photos: null,
  alternate_names: null,
  is_service_area_business: null,
  is_yelp_guaranteed: null,
  has_verified_license: null,
  ad_placement: null
)
```

