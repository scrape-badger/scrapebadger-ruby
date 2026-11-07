# ScrapeBadger::AutoScout24Api

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**autoscout24_check_autoscout24_health**](AutoScout24Api.md#autoscout24_check_autoscout24_health) | **GET** /v1/autoscout24/health | Check AutoScout24 health |
| [**autoscout24_list_markets**](AutoScout24Api.md#autoscout24_list_markets) | **GET** /v1/autoscout24/markets | List markets |
| [**autoscout24_list_search_filters**](AutoScout24Api.md#autoscout24_list_search_filters) | **GET** /v1/autoscout24/filters | List search filters |
| [**autoscout24_search_vehicles**](AutoScout24Api.md#autoscout24_search_vehicles) | **GET** /v1/autoscout24/search | Search vehicles |


## autoscout24_check_autoscout24_health

> Object autoscout24_check_autoscout24_health

Check AutoScout24 health

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

api_instance = ScrapeBadger::AutoScout24Api.new

begin
  # Check AutoScout24 health
  result = api_instance.autoscout24_check_autoscout24_health
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AutoScout24Api->autoscout24_check_autoscout24_health: #{e}"
end
```

#### Using the autoscout24_check_autoscout24_health_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> autoscout24_check_autoscout24_health_with_http_info

```ruby
begin
  # Check AutoScout24 health
  data, status_code, headers = api_instance.autoscout24_check_autoscout24_health_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AutoScout24Api->autoscout24_check_autoscout24_health_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## autoscout24_list_markets

> <AutoScout24MarketsResponse> autoscout24_list_markets

List markets

Verified marketplaces, domains, languages and currency. Free reference endpoint.

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

api_instance = ScrapeBadger::AutoScout24Api.new

begin
  # List markets
  result = api_instance.autoscout24_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AutoScout24Api->autoscout24_list_markets: #{e}"
end
```

#### Using the autoscout24_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AutoScout24MarketsResponse>, Integer, Hash)> autoscout24_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.autoscout24_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AutoScout24MarketsResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AutoScout24Api->autoscout24_list_markets_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AutoScout24MarketsResponse**](AutoScout24MarketsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## autoscout24_list_search_filters

> <AutoScout24FiltersResponse> autoscout24_list_search_filters(opts)

List search filters

Current native make, model and vehicle filter options. Set make for its models.

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

api_instance = ScrapeBadger::AutoScout24Api.new
opts = {
  market: 'de', # String | 
  make: 'make_example' # String | 
}

begin
  # List search filters
  result = api_instance.autoscout24_list_search_filters(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AutoScout24Api->autoscout24_list_search_filters: #{e}"
end
```

#### Using the autoscout24_list_search_filters_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AutoScout24FiltersResponse>, Integer, Hash)> autoscout24_list_search_filters_with_http_info(opts)

```ruby
begin
  # List search filters
  data, status_code, headers = api_instance.autoscout24_list_search_filters_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AutoScout24FiltersResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AutoScout24Api->autoscout24_list_search_filters_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** |  | [optional][default to &#39;de&#39;] |
| **make** | **String** |  | [optional] |

### Return type

[**AutoScout24FiltersResponse**](AutoScout24FiltersResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## autoscout24_search_vehicles

> <AutoScout24SearchResponse> autoscout24_search_vehicles(opts)

Search vehicles

Search live vehicle cards, seller/location information and current filter taxonomy.  Browsing is capped at 200 pages (normally 20 cards each). Narrow the query to reach more inventory. Empty results cost zero credits. Listing detail is not included in this API.

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

api_instance = ScrapeBadger::AutoScout24Api.new
opts = {
  market: 'de', # String | 
  make: 'make_example', # String | Native make slug, e.g. volkswagen or bmw.
  model: 'model_example', # String | Native model slug, e.g. golf. Requires make.
  price_min: 56, # Integer | 
  price_max: 56, # Integer | 
  mileage_min: 56, # Integer | Kilometres.
  mileage_max: 56, # Integer | 
  year_min: 56, # Integer | 
  year_max: 56, # Integer | 
  power_min: 56, # Integer | Engine power in kW.
  power_max: 56, # Integer | 
  fuel_type: 'petrol', # String | 
  transmission: 'automatic', # String | 
  body_type: 'compact', # String | 
  seller_type: 'dealer', # String | 
  condition: 'new', # String | 
  zip: 'zip_example', # String | Postal code in the requested market.
  radius: 56, # Integer | Kilometres; requires zip.
  sort_by: 'best_match', # String | 
  page: 56 # Integer | 
}

begin
  # Search vehicles
  result = api_instance.autoscout24_search_vehicles(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AutoScout24Api->autoscout24_search_vehicles: #{e}"
end
```

#### Using the autoscout24_search_vehicles_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AutoScout24SearchResponse>, Integer, Hash)> autoscout24_search_vehicles_with_http_info(opts)

```ruby
begin
  # Search vehicles
  data, status_code, headers = api_instance.autoscout24_search_vehicles_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AutoScout24SearchResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AutoScout24Api->autoscout24_search_vehicles_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** |  | [optional][default to &#39;de&#39;] |
| **make** | **String** | Native make slug, e.g. volkswagen or bmw. | [optional] |
| **model** | **String** | Native model slug, e.g. golf. Requires make. | [optional] |
| **price_min** | **Integer** |  | [optional] |
| **price_max** | **Integer** |  | [optional] |
| **mileage_min** | **Integer** | Kilometres. | [optional] |
| **mileage_max** | **Integer** |  | [optional] |
| **year_min** | **Integer** |  | [optional] |
| **year_max** | **Integer** |  | [optional] |
| **power_min** | **Integer** | Engine power in kW. | [optional] |
| **power_max** | **Integer** |  | [optional] |
| **fuel_type** | **String** |  | [optional] |
| **transmission** | **String** |  | [optional] |
| **body_type** | **String** |  | [optional] |
| **seller_type** | **String** |  | [optional] |
| **condition** | **String** |  | [optional] |
| **zip** | **String** | Postal code in the requested market. | [optional] |
| **radius** | **Integer** | Kilometres; requires zip. | [optional] |
| **sort_by** | **String** |  | [optional][default to &#39;best_match&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

[**AutoScout24SearchResponse**](AutoScout24SearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

