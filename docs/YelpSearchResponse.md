# ScrapeBadger::YelpSearchResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** |  |  |
| **query** | **String** |  |  |
| **location** | **String** |  |  |
| **location_resolved** | [**YelpResolvedLocation**](YelpResolvedLocation.md) |  |  |
| **did_you_mean** | **String** |  | [optional] |
| **query_matched** | **Boolean** | False when Yelp could not place the query; results are then Yelp&#39;s broader ranking for the location, as Yelp shows them. |  |
| **total_results** | **Integer** | Yelp&#39;s reported total; at most 110 are browsable. |  |
| **page** | **Integer** |  |  |
| **page_size** | **Integer** |  |  |
| **total_pages** | **Integer** |  |  |
| **has_next_page** | **Boolean** |  |  |
| **next_page** | **Integer** |  | [optional] |
| **results** | [**Array&lt;YelpBusiness&gt;**](YelpBusiness.md) |  |  |
| **ads** | [**Array&lt;YelpBusiness&gt;**](YelpBusiness.md) |  |  |
| **filters** | [**Hash&lt;String, YelpFilterGroup&gt;**](YelpFilterGroup.md) |  |  |
| **related_searches** | [**Array&lt;YelpLink&gt;**](YelpLink.md) |  |  |
| **source_url** | **String** |  |  |
| **fetched_at** | **String** |  |  |
| **fetched_utc** | **Float** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::YelpSearchResponse.new(
  market: null,
  query: null,
  location: null,
  location_resolved: null,
  did_you_mean: null,
  query_matched: null,
  total_results: null,
  page: null,
  page_size: null,
  total_pages: null,
  has_next_page: null,
  next_page: null,
  results: null,
  ads: null,
  filters: null,
  related_searches: null,
  source_url: null,
  fetched_at: null,
  fetched_utc: null
)
```

