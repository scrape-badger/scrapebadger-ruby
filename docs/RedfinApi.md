# ScrapeBadger::RedfinApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**redfin_get_agent_profile_listings**](RedfinApi.md#redfin_get_agent_profile_listings) | **GET** /v1/redfin/agent | Get agent profile + listings |
| [**redfin_get_property_detail**](RedfinApi.md#redfin_get_property_detail) | **GET** /v1/redfin/property/{property_id} | Get property detail |
| [**redfin_get_property_detail_by_url**](RedfinApi.md#redfin_get_property_detail_by_url) | **GET** /v1/redfin/property | Get property detail by URL |
| [**redfin_list_coverage_markets**](RedfinApi.md#redfin_list_coverage_markets) | **GET** /v1/redfin/markets | List coverage markets |
| [**redfin_redfin_scraper_health_check**](RedfinApi.md#redfin_redfin_scraper_health_check) | **GET** /v1/redfin/health | Redfin scraper health check |
| [**redfin_redfin_scraper_health_check_head**](RedfinApi.md#redfin_redfin_scraper_health_check_head) | **HEAD** /v1/redfin/health | Redfin scraper health check |
| [**redfin_region_address_suggestions**](RedfinApi.md#redfin_region_address_suggestions) | **GET** /v1/redfin/autocomplete | Region/address suggestions |
| [**redfin_search_properties**](RedfinApi.md#redfin_search_properties) | **GET** /v1/redfin/search | Search properties |


## redfin_get_agent_profile_listings

> Object redfin_get_agent_profile_listings(opts)

Get agent profile + listings

Get a Redfin real-estate agent's profile and their active listings.

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

api_instance = ScrapeBadger::RedfinApi.new
opts = {
  url: 'url_example', # String | Full Redfin /realestateagents/ URL
  agent_id: 'agent_id_example' # String | Redfin agent id
}

begin
  # Get agent profile + listings
  result = api_instance.redfin_get_agent_profile_listings(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_get_agent_profile_listings: #{e}"
end
```

#### Using the redfin_get_agent_profile_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> redfin_get_agent_profile_listings_with_http_info(opts)

```ruby
begin
  # Get agent profile + listings
  data, status_code, headers = api_instance.redfin_get_agent_profile_listings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_get_agent_profile_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Full Redfin /realestateagents/ URL | [optional] |
| **agent_id** | **String** | Redfin agent id | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## redfin_get_property_detail

> Object redfin_get_property_detail(property_id)

Get property detail

Get a single Redfin property's full detail by its numeric propertyId.

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

api_instance = ScrapeBadger::RedfinApi.new
property_id = 'property_id_example' # String | 

begin
  # Get property detail
  result = api_instance.redfin_get_property_detail(property_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_get_property_detail: #{e}"
end
```

#### Using the redfin_get_property_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> redfin_get_property_detail_with_http_info(property_id)

```ruby
begin
  # Get property detail
  data, status_code, headers = api_instance.redfin_get_property_detail_with_http_info(property_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_get_property_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **property_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## redfin_get_property_detail_by_url

> Object redfin_get_property_detail_by_url(url)

Get property detail by URL

Get a single Redfin property's full detail by its home URL.

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

api_instance = ScrapeBadger::RedfinApi.new
url = 'url_example' # String | Full Redfin property URL (/CA/City/.../home/12345678)

begin
  # Get property detail by URL
  result = api_instance.redfin_get_property_detail_by_url(url)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_get_property_detail_by_url: #{e}"
end
```

#### Using the redfin_get_property_detail_by_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> redfin_get_property_detail_by_url_with_http_info(url)

```ruby
begin
  # Get property detail by URL
  data, status_code, headers = api_instance.redfin_get_property_detail_by_url_with_http_info(url)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_get_property_detail_by_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Full Redfin property URL (/CA/City/.../home/12345678) |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## redfin_list_coverage_markets

> Object redfin_list_coverage_markets

List coverage markets

List Redfin coverage regions (US).

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

api_instance = ScrapeBadger::RedfinApi.new

begin
  # List coverage markets
  result = api_instance.redfin_list_coverage_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_list_coverage_markets: #{e}"
end
```

#### Using the redfin_list_coverage_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> redfin_list_coverage_markets_with_http_info

```ruby
begin
  # List coverage markets
  data, status_code, headers = api_instance.redfin_list_coverage_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_list_coverage_markets_with_http_info: #{e}"
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


## redfin_redfin_scraper_health_check

> Object redfin_redfin_scraper_health_check

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::RedfinApi.new

begin
  # Redfin scraper health check
  result = api_instance.redfin_redfin_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_redfin_scraper_health_check: #{e}"
end
```

#### Using the redfin_redfin_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> redfin_redfin_scraper_health_check_with_http_info

```ruby
begin
  # Redfin scraper health check
  data, status_code, headers = api_instance.redfin_redfin_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_redfin_scraper_health_check_with_http_info: #{e}"
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


## redfin_redfin_scraper_health_check_head

> Object redfin_redfin_scraper_health_check_head

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::RedfinApi.new

begin
  # Redfin scraper health check
  result = api_instance.redfin_redfin_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_redfin_scraper_health_check_head: #{e}"
end
```

#### Using the redfin_redfin_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> redfin_redfin_scraper_health_check_head_with_http_info

```ruby
begin
  # Redfin scraper health check
  data, status_code, headers = api_instance.redfin_redfin_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_redfin_scraper_health_check_head_with_http_info: #{e}"
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


## redfin_region_address_suggestions

> Object redfin_region_address_suggestions(query)

Region/address suggestions

Resolve a search term to Redfin regions/addresses.

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

api_instance = ScrapeBadger::RedfinApi.new
query = 'query_example' # String | Partial location — city, ZIP, address, neighborhood

begin
  # Region/address suggestions
  result = api_instance.redfin_region_address_suggestions(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_region_address_suggestions: #{e}"
end
```

#### Using the redfin_region_address_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> redfin_region_address_suggestions_with_http_info(query)

```ruby
begin
  # Region/address suggestions
  data, status_code, headers = api_instance.redfin_region_address_suggestions_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_region_address_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial location — city, ZIP, address, neighborhood |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## redfin_search_properties

> Object redfin_search_properties(location, opts)

Search properties

Search Redfin for for-sale / for-rent / recently-sold properties.

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

api_instance = ScrapeBadger::RedfinApi.new
location = 'location_example' # String | City/state, ZIP, address or neighborhood
opts = {
  page: 56, # Integer | 
  sort: 'sort_example', # String | relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths
  price_min: 56, # Integer | 
  price_max: 56, # Integer | 
  beds_min: 56, # Integer | 
  baths_min: 8.14, # Float | 
  home_type: 'home_type_example', # String | house|condo|townhouse|multi_family|land|mobile|coop|other
  sqft_min: 56, # Integer | 
  sqft_max: 56, # Integer | 
  lot_min: 56, # Integer | 
  lot_max: 56, # Integer | 
  year_built_min: 56, # Integer | 
  year_built_max: 56, # Integer | 
  max_days_on_market: 56, # Integer | 
  north: 8.14, # Float | Map bounds for tiling past the cap
  south: 8.14, # Float | 
  east: 8.14, # Float | 
  west: 8.14 # Float | 
}

begin
  # Search properties
  result = api_instance.redfin_search_properties(location, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_search_properties: #{e}"
end
```

#### Using the redfin_search_properties_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> redfin_search_properties_with_http_info(location, opts)

```ruby
begin
  # Search properties
  data, status_code, headers = api_instance.redfin_search_properties_with_http_info(location, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedfinApi->redfin_search_properties_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | City/state, ZIP, address or neighborhood |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **sort** | **String** | relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths | [optional] |
| **price_min** | **Integer** |  | [optional] |
| **price_max** | **Integer** |  | [optional] |
| **beds_min** | **Integer** |  | [optional] |
| **baths_min** | **Float** |  | [optional] |
| **home_type** | **String** | house|condo|townhouse|multi_family|land|mobile|coop|other | [optional] |
| **sqft_min** | **Integer** |  | [optional] |
| **sqft_max** | **Integer** |  | [optional] |
| **lot_min** | **Integer** |  | [optional] |
| **lot_max** | **Integer** |  | [optional] |
| **year_built_min** | **Integer** |  | [optional] |
| **year_built_max** | **Integer** |  | [optional] |
| **max_days_on_market** | **Integer** |  | [optional] |
| **north** | **Float** | Map bounds for tiling past the cap | [optional] |
| **south** | **Float** |  | [optional] |
| **east** | **Float** |  | [optional] |
| **west** | **Float** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

