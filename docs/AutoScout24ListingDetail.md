# ScrapeBadger::AutoScout24ListingDetail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **title** | **String** |  |  |
| **url** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **description_html** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **currency** | **String** |  | [optional][default to &#39;EUR&#39;] |
| **price** | **Float** |  | [optional] |
| **price_formatted** | **String** |  | [optional] |
| **net_price** | **Float** |  | [optional] |
| **vat_rate** | **Float** |  | [optional] |
| **is_vat_deductible** | **Boolean** |  | [optional] |
| **is_negotiable** | **Boolean** |  | [optional] |
| **is_price_on_request** | **Boolean** |  | [optional] |
| **is_final_price** | **Boolean** |  | [optional] |
| **median_price** | **Float** |  | [optional] |
| **price_evaluation** | **Integer** |  | [optional] |
| **price_details** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **prices** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **super_deal** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **make** | **String** |  | [optional] |
| **model** | **String** |  | [optional] |
| **variant** | **String** |  | [optional] |
| **version** | **String** |  | [optional] |
| **mileage_km** | **Integer** |  | [optional] |
| **first_registration** | **String** |  | [optional] |
| **registration_year** | **Integer** |  | [optional] |
| **registration_month** | **Integer** |  | [optional] |
| **power_kw** | **Float** |  | [optional] |
| **power_hp** | **Float** |  | [optional] |
| **displacement_cc** | **Integer** |  | [optional] |
| **transmission** | **String** |  | [optional] |
| **body_type** | **String** |  | [optional] |
| **fuel** | **String** |  | [optional] |
| **fuel_type** | **String** |  | [optional] |
| **seats** | **Integer** |  | [optional] |
| **doors** | **Integer** |  | [optional] |
| **vehicle** | **Hash&lt;String, Object&gt;** | Complete useful native specifications, including rawData, energy and history. | [optional] |
| **equipment** | **Hash&lt;String, Array&lt;Object&gt;&gt;** |  | [optional] |
| **images** | **Array&lt;String&gt;** |  | [optional] |
| **header_image** | **String** |  | [optional] |
| **image_alt_text** | **String** |  | [optional] |
| **is_cover_image_placeholder** | **Boolean** |  | [optional] |
| **cover_image_attractiveness** | **Float** |  | [optional] |
| **youtube_link** | **String** |  | [optional] |
| **twinner_url** | **String** |  | [optional] |
| **has_360_view** | **Boolean** |  | [optional] |
| **three_sixty** | **Object** |  | [optional] |
| **vehicle_report** | **Object** |  | [optional] |
| **partner_integrations** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |
| **seller** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **location** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **ratings** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **rating** | **Float** |  | [optional] |
| **rating_count** | **Integer** |  | [optional] |
| **recommend_percentage** | **Float** |  | [optional] |
| **whatsapp_number** | **String** |  | [optional] |
| **identifier** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **article_type** | **String** |  | [optional] |
| **vehicle_type** | **String** |  | [optional] |
| **is_new** | **Boolean** |  | [optional] |
| **is_deliverable** | **Boolean** |  | [optional] |
| **availability** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **available_at** | **String** |  | [optional] |
| **available_utc** | **Float** |  | [optional] |
| **created_at** | **String** |  | [optional] |
| **created_utc** | **Float** |  | [optional] |
| **leasing_details** | **Object** |  | [optional] |
| **warranty** | **Object** |  | [optional] |
| **has_warranty** | **Boolean** |  | [optional] |
| **financing_flags** | **Object** |  | [optional] |
| **financing_and_insurance** | **Object** |  | [optional] |
| **online_purchase** | **Object** |  | [optional] |
| **seals** | **Array&lt;Object&gt;** |  | [optional] |
| **special_conditions** | **Array&lt;Object&gt;** |  | [optional] |
| **search_result_type** | **String** |  | [optional] |
| **ad_tier** | **String** |  | [optional] |
| **applied_ad_tier** | **String** |  | [optional] |
| **has_premium_listing_treatment** | **Boolean** |  | [optional] |
| **is_trending** | **Boolean** |  | [optional] |
| **is_listing_boost** | **Boolean** |  | [optional] |
| **statistics** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **interaction_statistics** | **Hash&lt;String, Object&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::AutoScout24ListingDetail.new(
  id: null,
  title: null,
  url: null,
  description: null,
  description_html: null,
  status: null,
  currency: null,
  price: null,
  price_formatted: null,
  net_price: null,
  vat_rate: null,
  is_vat_deductible: null,
  is_negotiable: null,
  is_price_on_request: null,
  is_final_price: null,
  median_price: null,
  price_evaluation: null,
  price_details: null,
  prices: null,
  super_deal: null,
  make: null,
  model: null,
  variant: null,
  version: null,
  mileage_km: null,
  first_registration: null,
  registration_year: null,
  registration_month: null,
  power_kw: null,
  power_hp: null,
  displacement_cc: null,
  transmission: null,
  body_type: null,
  fuel: null,
  fuel_type: null,
  seats: null,
  doors: null,
  vehicle: null,
  equipment: null,
  images: null,
  header_image: null,
  image_alt_text: null,
  is_cover_image_placeholder: null,
  cover_image_attractiveness: null,
  youtube_link: null,
  twinner_url: null,
  has_360_view: null,
  three_sixty: null,
  vehicle_report: null,
  partner_integrations: null,
  seller: null,
  location: null,
  ratings: null,
  rating: null,
  rating_count: null,
  recommend_percentage: null,
  whatsapp_number: null,
  identifier: null,
  article_type: null,
  vehicle_type: null,
  is_new: null,
  is_deliverable: null,
  availability: null,
  available_at: null,
  available_utc: null,
  created_at: null,
  created_utc: null,
  leasing_details: null,
  warranty: null,
  has_warranty: null,
  financing_flags: null,
  financing_and_insurance: null,
  online_purchase: null,
  seals: null,
  special_conditions: null,
  search_result_type: null,
  ad_tier: null,
  applied_ad_tier: null,
  has_premium_listing_treatment: null,
  is_trending: null,
  is_listing_boost: null,
  statistics: null,
  interaction_statistics: null
)
```

