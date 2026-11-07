# ScrapeBadger::YelpApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**yelp_list_markets**](YelpApi.md#yelp_list_markets) | **GET** /v1/yelp/markets | List markets |
| [**yelp_search_businesses**](YelpApi.md#yelp_search_businesses) | **GET** /v1/yelp/search | Search businesses |


## yelp_list_markets

> <YelpMarketsResponse> yelp_list_markets

List markets

Yelp sites this API verifiably searches. Free.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::YelpApi.new

begin
  # List markets
  result = api_instance.yelp_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YelpApi->yelp_list_markets: #{e}"
end
```

#### Using the yelp_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<YelpMarketsResponse>, Integer, Hash)> yelp_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.yelp_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <YelpMarketsResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YelpApi->yelp_list_markets_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**YelpMarketsResponse**](YelpMarketsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## yelp_search_businesses

> <YelpSearchResponse> yelp_search_businesses(location, opts)

Search businesses

Ranked Yelp businesses for a location, with ads kept separate. 15 credits; empty results free.  Ten businesses per page, pages 1-11. Narrow the location, category or filters to reach more businesses. Business detail and reviews are not part of this API.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::YelpApi.new
location = 'location_example' # String | Where to search, as typed into Yelp: city, neighbourhood, address or postcode.
opts = {
  query: 'query_example', # String | What to search for (e.g. pizza, plumbers). Optional when category is set.
  market: 'us', # String | Yelp site to search; see /markets.
  category: 'category_example', # String | Yelp category alias, e.g. pizza, coffee, plumbing.
  sort_by: 'recommended', # String | 
  price: 'price_example', # String | Comma-separated price levels 1-4 ($ to $$$$).
  features: 'features_example', # String | Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible.
  page: 56 # Integer | 1-based page, ten businesses each; pages 1-11.
}

begin
  # Search businesses
  result = api_instance.yelp_search_businesses(location, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YelpApi->yelp_search_businesses: #{e}"
end
```

#### Using the yelp_search_businesses_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<YelpSearchResponse>, Integer, Hash)> yelp_search_businesses_with_http_info(location, opts)

```ruby
begin
  # Search businesses
  data, status_code, headers = api_instance.yelp_search_businesses_with_http_info(location, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <YelpSearchResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YelpApi->yelp_search_businesses_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | Where to search, as typed into Yelp: city, neighbourhood, address or postcode. |  |
| **query** | **String** | What to search for (e.g. pizza, plumbers). Optional when category is set. | [optional] |
| **market** | **String** | Yelp site to search; see /markets. | [optional][default to &#39;us&#39;] |
| **category** | **String** | Yelp category alias, e.g. pizza, coffee, plumbing. | [optional] |
| **sort_by** | **String** |  | [optional][default to &#39;recommended&#39;] |
| **price** | **String** | Comma-separated price levels 1-4 ($ to $$$$). | [optional] |
| **features** | **String** | Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible. | [optional] |
| **page** | **Integer** | 1-based page, ten businesses each; pages 1-11. | [optional][default to 1] |

### Return type

[**YelpSearchResponse**](YelpSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

