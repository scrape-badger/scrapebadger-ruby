# ScrapeBadger::LoopNetApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**loopnet_get_broker_profile**](LoopNetApi.md#loopnet_get_broker_profile) | **GET** /v1/loopnet/brokers/{slug}/{broker_id} | Get broker profile |
| [**loopnet_get_listing_detail**](LoopNetApi.md#loopnet_get_listing_detail) | **GET** /v1/loopnet/listings/{listing_id} | Get listing detail |
| [**loopnet_list_coverage_markets**](LoopNetApi.md#loopnet_list_coverage_markets) | **GET** /v1/loopnet/markets | List coverage markets |
| [**loopnet_list_property_types**](LoopNetApi.md#loopnet_list_property_types) | **GET** /v1/loopnet/property-types | List property types |
| [**loopnet_loopnet_scraper_health_check**](LoopNetApi.md#loopnet_loopnet_scraper_health_check) | **GET** /v1/loopnet/health | LoopNet scraper health check |
| [**loopnet_loopnet_scraper_health_check_head**](LoopNetApi.md#loopnet_loopnet_scraper_health_check_head) | **HEAD** /v1/loopnet/health | LoopNet scraper health check |
| [**loopnet_search_commercial_real_estate**](LoopNetApi.md#loopnet_search_commercial_real_estate) | **GET** /v1/loopnet/search | Search commercial real estate |


## loopnet_get_broker_profile

> Object loopnet_get_broker_profile(slug, broker_id, opts)

Get broker profile

Get a LoopNet broker profile + their listings by slug + id.

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

api_instance = ScrapeBadger::LoopNetApi.new
slug = 'slug_example' # String | 
broker_id = 'broker_id_example' # String | 
opts = {
  market: 'market_example' # String | us|ca|uk|fr|es
}

begin
  # Get broker profile
  result = api_instance.loopnet_get_broker_profile(slug, broker_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_get_broker_profile: #{e}"
end
```

#### Using the loopnet_get_broker_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> loopnet_get_broker_profile_with_http_info(slug, broker_id, opts)

```ruby
begin
  # Get broker profile
  data, status_code, headers = api_instance.loopnet_get_broker_profile_with_http_info(slug, broker_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_get_broker_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **slug** | **String** |  |  |
| **broker_id** | **String** |  |  |
| **market** | **String** | us|ca|uk|fr|es | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## loopnet_get_listing_detail

> Object loopnet_get_listing_detail(listing_id, opts)

Get listing detail

Get a single LoopNet listing's full detail by its numeric id.

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

api_instance = ScrapeBadger::LoopNetApi.new
listing_id = 'listing_id_example' # String | 
opts = {
  market: 'market_example' # String | us|ca|uk|fr|es
}

begin
  # Get listing detail
  result = api_instance.loopnet_get_listing_detail(listing_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_get_listing_detail: #{e}"
end
```

#### Using the loopnet_get_listing_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> loopnet_get_listing_detail_with_http_info(listing_id, opts)

```ruby
begin
  # Get listing detail
  data, status_code, headers = api_instance.loopnet_get_listing_detail_with_http_info(listing_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_get_listing_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **listing_id** | **String** |  |  |
| **market** | **String** | us|ca|uk|fr|es | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## loopnet_list_coverage_markets

> Object loopnet_list_coverage_markets

List coverage markets

List LoopNet coverage markets (US, CA, UK, FR, ES).

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

api_instance = ScrapeBadger::LoopNetApi.new

begin
  # List coverage markets
  result = api_instance.loopnet_list_coverage_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_list_coverage_markets: #{e}"
end
```

#### Using the loopnet_list_coverage_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> loopnet_list_coverage_markets_with_http_info

```ruby
begin
  # List coverage markets
  data, status_code, headers = api_instance.loopnet_list_coverage_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_list_coverage_markets_with_http_info: #{e}"
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


## loopnet_list_property_types

> Object loopnet_list_property_types

List property types

List LoopNet property-type facets accepted by /search.

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

api_instance = ScrapeBadger::LoopNetApi.new

begin
  # List property types
  result = api_instance.loopnet_list_property_types
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_list_property_types: #{e}"
end
```

#### Using the loopnet_list_property_types_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> loopnet_list_property_types_with_http_info

```ruby
begin
  # List property types
  data, status_code, headers = api_instance.loopnet_list_property_types_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_list_property_types_with_http_info: #{e}"
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


## loopnet_loopnet_scraper_health_check

> Object loopnet_loopnet_scraper_health_check

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::LoopNetApi.new

begin
  # LoopNet scraper health check
  result = api_instance.loopnet_loopnet_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_loopnet_scraper_health_check: #{e}"
end
```

#### Using the loopnet_loopnet_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> loopnet_loopnet_scraper_health_check_with_http_info

```ruby
begin
  # LoopNet scraper health check
  data, status_code, headers = api_instance.loopnet_loopnet_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_loopnet_scraper_health_check_with_http_info: #{e}"
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


## loopnet_loopnet_scraper_health_check_head

> Object loopnet_loopnet_scraper_health_check_head

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::LoopNetApi.new

begin
  # LoopNet scraper health check
  result = api_instance.loopnet_loopnet_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_loopnet_scraper_health_check_head: #{e}"
end
```

#### Using the loopnet_loopnet_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> loopnet_loopnet_scraper_health_check_head_with_http_info

```ruby
begin
  # LoopNet scraper health check
  data, status_code, headers = api_instance.loopnet_loopnet_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_loopnet_scraper_health_check_head_with_http_info: #{e}"
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


## loopnet_search_commercial_real_estate

> Object loopnet_search_commercial_real_estate(location, opts)

Search commercial real estate

Search LoopNet for-lease / for-sale / auction listings across all markets.

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

api_instance = ScrapeBadger::LoopNetApi.new
location = 'location_example' # String | City/state, ZIP, state code, or 'usa'
opts = {
  market: 'market_example', # String | us|ca|uk|fr|es
  listing_type: 'listing_type_example', # String | for-lease|for-sale|auctions
  property_type: 'property_type_example', # String | Slug from /property-types
  page: 56, # Integer | 
  min_price: 56, # Integer | 
  max_price: 56, # Integer | 
  price_type: 'price_type_example', # String | unit | sf | acre
  min_size: 56, # Integer | 
  max_size: 56 # Integer | 
}

begin
  # Search commercial real estate
  result = api_instance.loopnet_search_commercial_real_estate(location, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_search_commercial_real_estate: #{e}"
end
```

#### Using the loopnet_search_commercial_real_estate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> loopnet_search_commercial_real_estate_with_http_info(location, opts)

```ruby
begin
  # Search commercial real estate
  data, status_code, headers = api_instance.loopnet_search_commercial_real_estate_with_http_info(location, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LoopNetApi->loopnet_search_commercial_real_estate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | City/state, ZIP, state code, or &#39;usa&#39; |  |
| **market** | **String** | us|ca|uk|fr|es | [optional][default to &#39;us&#39;] |
| **listing_type** | **String** | for-lease|for-sale|auctions | [optional][default to &#39;for-lease&#39;] |
| **property_type** | **String** | Slug from /property-types | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **min_price** | **Integer** |  | [optional] |
| **max_price** | **Integer** |  | [optional] |
| **price_type** | **String** | unit | sf | acre | [optional] |
| **min_size** | **Integer** |  | [optional] |
| **max_size** | **Integer** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

