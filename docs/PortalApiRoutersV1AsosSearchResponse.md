# ScrapeBadger::PortalApiRoutersV1AsosSearchResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** |  |  |
| **search_term** | [**Searchterm**](Searchterm.md) |  | [optional] |
| **category_name** | [**Categoryname**](Categoryname.md) |  | [optional] |
| **total_results** | **Integer** |  |  |
| **offset** | **Integer** |  |  |
| **limit** | **Integer** |  |  |
| **next_offset** | [**NextOffset**](NextOffset.md) |  | [optional] |
| **products** | [**Array&lt;Product&gt;**](Product.md) |  |  |
| **facets** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::PortalApiRoutersV1AsosSearchResponse.new(
  market: null,
  search_term: null,
  category_name: null,
  total_results: null,
  offset: null,
  limit: null,
  next_offset: null,
  products: null,
  facets: null
)
```

