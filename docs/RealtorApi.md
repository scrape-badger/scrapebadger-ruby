# ScrapeBadger::RealtorApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**realtor_get_full_property_detail**](RealtorApi.md#realtor_get_full_property_detail) | **GET** /v1/realtor/properties/{property_id} | Get full property detail |
| [**realtor_list_markets**](RealtorApi.md#realtor_list_markets) | **GET** /v1/realtor/markets | List markets |
| [**realtor_location_autocomplete**](RealtorApi.md#realtor_location_autocomplete) | **GET** /v1/realtor/autocomplete | Location autocomplete |
| [**realtor_realtor_scraper_health_check**](RealtorApi.md#realtor_realtor_scraper_health_check) | **GET** /v1/realtor/health | Realtor scraper health check |
| [**realtor_realtor_scraper_health_check_head**](RealtorApi.md#realtor_realtor_scraper_health_check_head) | **HEAD** /v1/realtor/health | Realtor scraper health check |
| [**realtor_search_property_listings**](RealtorApi.md#realtor_search_property_listings) | **GET** /v1/realtor/search | Search property listings |


## realtor_get_full_property_detail

> Object realtor_get_full_property_detail(property_id, opts)

Get full property detail

Full listing detail: features, tax & price history, schools, photos, agents.

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

api_instance = ScrapeBadger::RealtorApi.new
property_id = 'property_id_example' # String | 
opts = {
  market: 'market_example' # String | us (realtor.com) | ca (realtor.ca)
}

begin
  # Get full property detail
  result = api_instance.realtor_get_full_property_detail(property_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_get_full_property_detail: #{e}"
end
```

#### Using the realtor_get_full_property_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> realtor_get_full_property_detail_with_http_info(property_id, opts)

```ruby
begin
  # Get full property detail
  data, status_code, headers = api_instance.realtor_get_full_property_detail_with_http_info(property_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_get_full_property_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **property_id** | **String** |  |  |
| **market** | **String** | us (realtor.com) | ca (realtor.ca) | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## realtor_list_markets

> Object realtor_list_markets

List markets

List supported Realtor markets (US = realtor.com, CA = realtor.ca).

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

api_instance = ScrapeBadger::RealtorApi.new

begin
  # List markets
  result = api_instance.realtor_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_list_markets: #{e}"
end
```

#### Using the realtor_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> realtor_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.realtor_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_list_markets_with_http_info: #{e}"
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


## realtor_location_autocomplete

> Object realtor_location_autocomplete(query, opts)

Location autocomplete

Resolve a location query into candidate places to feed /search.

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

api_instance = ScrapeBadger::RealtorApi.new
query = 'query_example' # String | Freetext location (city, ZIP/postal, address…)
opts = {
  market: 'market_example', # String | us (realtor.com) | ca (realtor.ca)
  limit: 56 # Integer | 
}

begin
  # Location autocomplete
  result = api_instance.realtor_location_autocomplete(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_location_autocomplete: #{e}"
end
```

#### Using the realtor_location_autocomplete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> realtor_location_autocomplete_with_http_info(query, opts)

```ruby
begin
  # Location autocomplete
  data, status_code, headers = api_instance.realtor_location_autocomplete_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_location_autocomplete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Freetext location (city, ZIP/postal, address…) |  |
| **market** | **String** | us (realtor.com) | ca (realtor.ca) | [optional][default to &#39;us&#39;] |
| **limit** | **Integer** |  | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## realtor_realtor_scraper_health_check

> Object realtor_realtor_scraper_health_check

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::RealtorApi.new

begin
  # Realtor scraper health check
  result = api_instance.realtor_realtor_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_realtor_scraper_health_check: #{e}"
end
```

#### Using the realtor_realtor_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> realtor_realtor_scraper_health_check_with_http_info

```ruby
begin
  # Realtor scraper health check
  data, status_code, headers = api_instance.realtor_realtor_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_realtor_scraper_health_check_with_http_info: #{e}"
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


## realtor_realtor_scraper_health_check_head

> Object realtor_realtor_scraper_health_check_head

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::RealtorApi.new

begin
  # Realtor scraper health check
  result = api_instance.realtor_realtor_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_realtor_scraper_health_check_head: #{e}"
end
```

#### Using the realtor_realtor_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> realtor_realtor_scraper_health_check_head_with_http_info

```ruby
begin
  # Realtor scraper health check
  data, status_code, headers = api_instance.realtor_realtor_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_realtor_scraper_health_check_head_with_http_info: #{e}"
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


## realtor_search_property_listings

> Object realtor_search_property_listings(opts)

Search property listings

Search for-sale/for-rent/sold listings with rich filters.

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

api_instance = ScrapeBadger::RealtorApi.new
opts = {
  location: 'location_example', # String | 'Austin, TX', a ZIP, 'Toronto, ON'…
  market: 'market_example', # String | us (realtor.com) | ca (realtor.ca)
  status: 'status_example', # String | for_sale | for_rent | sold | pending
  price_min: 8.14, # Float | 
  price_max: 8.14, # Float | 
  beds_min: 56, # Integer | 
  baths_min: 56, # Integer | 
  sqft_min: 56, # Integer | US only
  sqft_max: 56, # Integer | US only
  property_type: 'property_type_example', # String | US only, CSV of property types
  sort: 'sort_example', # String | relevant | newest | price_low | price_high | photo_count
  page: 56, # Integer | 
  limit: 56, # Integer | 
  lat_min: 8.14, # Float | CA bbox south
  lat_max: 8.14, # Float | CA bbox north
  lng_min: 8.14, # Float | CA bbox west
  lng_max: 8.14 # Float | CA bbox east
}

begin
  # Search property listings
  result = api_instance.realtor_search_property_listings(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_search_property_listings: #{e}"
end
```

#### Using the realtor_search_property_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> realtor_search_property_listings_with_http_info(opts)

```ruby
begin
  # Search property listings
  data, status_code, headers = api_instance.realtor_search_property_listings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RealtorApi->realtor_search_property_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | &#39;Austin, TX&#39;, a ZIP, &#39;Toronto, ON&#39;… | [optional] |
| **market** | **String** | us (realtor.com) | ca (realtor.ca) | [optional][default to &#39;us&#39;] |
| **status** | **String** | for_sale | for_rent | sold | pending | [optional][default to &#39;for_sale&#39;] |
| **price_min** | **Float** |  | [optional] |
| **price_max** | **Float** |  | [optional] |
| **beds_min** | **Integer** |  | [optional] |
| **baths_min** | **Integer** |  | [optional] |
| **sqft_min** | **Integer** | US only | [optional] |
| **sqft_max** | **Integer** | US only | [optional] |
| **property_type** | **String** | US only, CSV of property types | [optional] |
| **sort** | **String** | relevant | newest | price_low | price_high | photo_count | [optional][default to &#39;relevant&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **limit** | **Integer** |  | [optional] |
| **lat_min** | **Float** | CA bbox south | [optional] |
| **lat_max** | **Float** | CA bbox north | [optional] |
| **lng_min** | **Float** | CA bbox west | [optional] |
| **lng_max** | **Float** | CA bbox east | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

