# ScrapeBadger::AutoScout24Listing

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **cross_reference_id** | **String** |  | [optional] |
| **position** | **Integer** |  |  |
| **title** | **String** |  |  |
| **url** | **String** |  |  |
| **images** | **Array&lt;String&gt;** |  | [optional] |
| **online_purchase_images** | **Array&lt;String&gt;** |  | [optional] |
| **price** | **Float** |  | [optional] |
| **currency** | **String** |  | [optional][default to &#39;EUR&#39;] |
| **price_formatted** | **String** |  | [optional] |
| **price_evaluation** | **Integer** |  | [optional] |
| **price_evaluation_enabled** | **Boolean** |  | [optional] |
| **price_details** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **old_price_formatted** | **String** |  | [optional] |
| **is_super_deal** | **Boolean** |  | [optional] |
| **is_conditional_price** | **Boolean** |  | [optional] |
| **vat_label_required** | **Boolean** |  | [optional] |
| **make** | **String** |  | [optional] |
| **model** | **String** |  | [optional] |
| **model_id** | **Integer** |  | [optional] |
| **model_group** | **String** |  | [optional] |
| **variant** | **String** |  | [optional] |
| **motor_type** | **String** |  | [optional] |
| **version** | **String** |  | [optional] |
| **subtitle** | **String** |  | [optional] |
| **article_type** | **String** |  | [optional] |
| **offer_type** | **String** |  | [optional] |
| **fuel** | **String** |  | [optional] |
| **fuel_type** | **String** |  | [optional] |
| **transmission** | **String** |  | [optional] |
| **mileage_km** | **Integer** |  | [optional] |
| **first_registration** | **String** |  | [optional] |
| **registration_year** | **Integer** |  | [optional] |
| **registration_month** | **Integer** |  | [optional] |
| **power_kw** | **Float** |  | [optional] |
| **power_hp** | **Float** |  | [optional] |
| **displacement_cc** | **Integer** |  | [optional] |
| **is_damaged** | **Boolean** |  | [optional] |
| **available_now** | **Boolean** |  | [optional] |
| **available_at** | **String** |  | [optional] |
| **available_utc** | **Float** |  | [optional] |
| **availability_in_days** | **Integer** |  | [optional] |
| **location** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **seller** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **rating** | **Float** |  | [optional] |
| **rating_count** | **Integer** |  | [optional] |
| **ratings_enabled** | **Boolean** |  | [optional] |
| **leasing** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **seals** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |
| **online_purchase** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **electric_vehicle_banner** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **is_deliverable** | **Boolean** |  | [optional] |
| **has_video** | **Boolean** |  | [optional] |
| **has_360_image** | **Boolean** |  | [optional] |
| **interest_level** | **String** |  | [optional] |
| **is_trending** | **Boolean** |  | [optional] |
| **ad_tier** | **String** |  | [optional] |
| **result_type** | **String** |  | [optional] |
| **result_section** | **String** |  | [optional] |
| **special_conditions** | **Array&lt;Object&gt;** |  | [optional] |
| **vehicle_details** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |
| **wltp_values** | **Array&lt;String&gt;** |  | [optional] |
| **vehicle** | **Hash&lt;String, Object&gt;** | Additional native vehicle attributes, including localized labels. | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::AutoScout24Listing.new(
  id: null,
  cross_reference_id: null,
  position: null,
  title: null,
  url: null,
  images: null,
  online_purchase_images: null,
  price: null,
  currency: null,
  price_formatted: null,
  price_evaluation: null,
  price_evaluation_enabled: null,
  price_details: null,
  old_price_formatted: null,
  is_super_deal: null,
  is_conditional_price: null,
  vat_label_required: null,
  make: null,
  model: null,
  model_id: null,
  model_group: null,
  variant: null,
  motor_type: null,
  version: null,
  subtitle: null,
  article_type: null,
  offer_type: null,
  fuel: null,
  fuel_type: null,
  transmission: null,
  mileage_km: null,
  first_registration: null,
  registration_year: null,
  registration_month: null,
  power_kw: null,
  power_hp: null,
  displacement_cc: null,
  is_damaged: null,
  available_now: null,
  available_at: null,
  available_utc: null,
  availability_in_days: null,
  location: null,
  seller: null,
  rating: null,
  rating_count: null,
  ratings_enabled: null,
  leasing: null,
  seals: null,
  online_purchase: null,
  electric_vehicle_banner: null,
  is_deliverable: null,
  has_video: null,
  has_360_image: null,
  interest_level: null,
  is_trending: null,
  ad_tier: null,
  result_type: null,
  result_section: null,
  special_conditions: null,
  vehicle_details: null,
  wltp_values: null,
  vehicle: null
)
```

