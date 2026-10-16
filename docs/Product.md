# ScrapeBadger::Product

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **name** | **String** |  |  |
| **product_code** | [**Productcode**](Productcode.md) |  | [optional] |
| **brand_name** | [**Brandname**](Brandname.md) |  | [optional] |
| **brand_id** | [**Brandid**](Brandid.md) |  | [optional] |
| **colour** | [**Colour**](Colour.md) |  | [optional] |
| **colour_way_id** | [**Colourwayid**](Colourwayid.md) |  | [optional] |
| **price** | [**ProductPrice**](ProductPrice.md) |  | [optional] |
| **url** | [**Url**](Url.md) |  | [optional] |
| **image_url** | [**Imageurl**](Imageurl.md) |  | [optional] |
| **additional_image_urls** | **Array&lt;String&gt;** |  | [optional] |
| **images** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |
| **variants** | [**Array&lt;Variant&gt;**](Variant.md) |  | [optional] |
| **is_selling_fast** | [**Issellingfast**](Issellingfast.md) |  | [optional] |
| **is_restocking_soon** | [**Isrestockingsoon**](Isrestockingsoon.md) |  | [optional] |
| **is_in_stock** | [**Isinstock**](Isinstock.md) |  | [optional] |
| **gender** | [**Gender**](Gender.md) |  | [optional] |
| **description** | [**Description**](Description.md) |  | [optional] |
| **ratings** | [**Ratings**](Ratings.md) |  | [optional] |
| **breadcrumbs** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::Product.new(
  id: null,
  name: null,
  product_code: null,
  brand_name: null,
  brand_id: null,
  colour: null,
  colour_way_id: null,
  price: null,
  url: null,
  image_url: null,
  additional_image_urls: null,
  images: null,
  variants: null,
  is_selling_fast: null,
  is_restocking_soon: null,
  is_in_stock: null,
  gender: null,
  description: null,
  ratings: null,
  breadcrumbs: null
)
```

