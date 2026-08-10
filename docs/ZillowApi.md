# ScrapeBadger::ZillowApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**zillow_get_agent_profile_listings**](ZillowApi.md#zillow_get_agent_profile_listings) | **GET** /v1/zillow/agent | Get agent profile + listings |
| [**zillow_get_property_detail**](ZillowApi.md#zillow_get_property_detail) | **GET** /v1/zillow/property/{zpid} | Get property detail |
| [**zillow_get_property_detail_by_url**](ZillowApi.md#zillow_get_property_detail_by_url) | **GET** /v1/zillow/property | Get property detail by URL |
| [**zillow_list_coverage_markets**](ZillowApi.md#zillow_list_coverage_markets) | **GET** /v1/zillow/markets | List coverage markets |
| [**zillow_region_address_suggestions**](ZillowApi.md#zillow_region_address_suggestions) | **GET** /v1/zillow/autocomplete | Region/address suggestions |
| [**zillow_search_properties**](ZillowApi.md#zillow_search_properties) | **GET** /v1/zillow/search | Search properties |
| [**zillow_zillow_scraper_health_check**](ZillowApi.md#zillow_zillow_scraper_health_check) | **GET** /v1/zillow/health | Zillow scraper health check |
| [**zillow_zillow_scraper_health_check_head**](ZillowApi.md#zillow_zillow_scraper_health_check_head) | **HEAD** /v1/zillow/health | Zillow scraper health check |


## zillow_get_agent_profile_listings

> Object zillow_get_agent_profile_listings(opts)

Get agent profile + listings

Get a Zillow professional's profile and their active listings.

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

api_instance = ScrapeBadger::ZillowApi.new
opts = {
  username: 'username_example', # String | Zillow profile username
  url: 'url_example' # String | Full Zillow /profile/... URL
}

begin
  # Get agent profile + listings
  result = api_instance.zillow_get_agent_profile_listings(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_get_agent_profile_listings: #{e}"
end
```

#### Using the zillow_get_agent_profile_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> zillow_get_agent_profile_listings_with_http_info(opts)

```ruby
begin
  # Get agent profile + listings
  data, status_code, headers = api_instance.zillow_get_agent_profile_listings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_get_agent_profile_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** | Zillow profile username | [optional] |
| **url** | **String** | Full Zillow /profile/... URL | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## zillow_get_property_detail

> Object zillow_get_property_detail(zpid)

Get property detail

Get a single Zillow property's full detail by zpid.

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

api_instance = ScrapeBadger::ZillowApi.new
zpid = 'zpid_example' # String | 

begin
  # Get property detail
  result = api_instance.zillow_get_property_detail(zpid)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_get_property_detail: #{e}"
end
```

#### Using the zillow_get_property_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> zillow_get_property_detail_with_http_info(zpid)

```ruby
begin
  # Get property detail
  data, status_code, headers = api_instance.zillow_get_property_detail_with_http_info(zpid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_get_property_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **zpid** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## zillow_get_property_detail_by_url

> Object zillow_get_property_detail_by_url(url)

Get property detail by URL

Get a single Zillow property's full detail by its homedetails URL.

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

api_instance = ScrapeBadger::ZillowApi.new
url = 'url_example' # String | Full Zillow /homedetails/... URL

begin
  # Get property detail by URL
  result = api_instance.zillow_get_property_detail_by_url(url)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_get_property_detail_by_url: #{e}"
end
```

#### Using the zillow_get_property_detail_by_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> zillow_get_property_detail_by_url_with_http_info(url)

```ruby
begin
  # Get property detail by URL
  data, status_code, headers = api_instance.zillow_get_property_detail_by_url_with_http_info(url)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_get_property_detail_by_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Full Zillow /homedetails/... URL |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## zillow_list_coverage_markets

> Object zillow_list_coverage_markets

List coverage markets

List Zillow coverage regions (US + Canada).

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

api_instance = ScrapeBadger::ZillowApi.new

begin
  # List coverage markets
  result = api_instance.zillow_list_coverage_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_list_coverage_markets: #{e}"
end
```

#### Using the zillow_list_coverage_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> zillow_list_coverage_markets_with_http_info

```ruby
begin
  # List coverage markets
  data, status_code, headers = api_instance.zillow_list_coverage_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_list_coverage_markets_with_http_info: #{e}"
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


## zillow_region_address_suggestions

> Object zillow_region_address_suggestions(query)

Region/address suggestions

Resolve a search term to Zillow regions/addresses.

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

api_instance = ScrapeBadger::ZillowApi.new
query = 'query_example' # String | Partial location — city, ZIP, address, neighborhood

begin
  # Region/address suggestions
  result = api_instance.zillow_region_address_suggestions(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_region_address_suggestions: #{e}"
end
```

#### Using the zillow_region_address_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> zillow_region_address_suggestions_with_http_info(query)

```ruby
begin
  # Region/address suggestions
  data, status_code, headers = api_instance.zillow_region_address_suggestions_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_region_address_suggestions_with_http_info: #{e}"
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


## zillow_search_properties

> Object zillow_search_properties(location, opts)

Search properties

Search Zillow for for-sale / for-rent / recently-sold properties.

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

api_instance = ScrapeBadger::ZillowApi.new
location = 'location_example' # String | City/state, ZIP, address or neighborhood
opts = {
  status: 'status_example', # String | for_sale|for_rent|sold
  page: 56, # Integer | 
  sort: 'sort_example', # String | homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built
  price_min: 56, # Integer | 
  price_max: 56, # Integer | 
  beds_min: 56, # Integer | 
  baths_min: 8.14, # Float | 
  home_type: 'home_type_example', # String | houses|condos|townhomes|apartments|manufactured|lots|multi_family
  sqft_min: 56, # Integer | 
  sqft_max: 56, # Integer | 
  lot_min: 56, # Integer | 
  lot_max: 56, # Integer | 
  year_built_min: 56, # Integer | 
  year_built_max: 56, # Integer | 
  hoa_max: 56, # Integer | 
  keywords: 'keywords_example', # String | 
  days_on: 'days_on_example', # String | 
  north: 8.14, # Float | Map bounds for tiling past the 820 cap
  south: 8.14, # Float | 
  east: 8.14, # Float | 
  west: 8.14 # Float | 
}

begin
  # Search properties
  result = api_instance.zillow_search_properties(location, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_search_properties: #{e}"
end
```

#### Using the zillow_search_properties_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> zillow_search_properties_with_http_info(location, opts)

```ruby
begin
  # Search properties
  data, status_code, headers = api_instance.zillow_search_properties_with_http_info(location, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_search_properties_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | City/state, ZIP, address or neighborhood |  |
| **status** | **String** | for_sale|for_rent|sold | [optional][default to &#39;for_sale&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **sort** | **String** | homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built | [optional] |
| **price_min** | **Integer** |  | [optional] |
| **price_max** | **Integer** |  | [optional] |
| **beds_min** | **Integer** |  | [optional] |
| **baths_min** | **Float** |  | [optional] |
| **home_type** | **String** | houses|condos|townhomes|apartments|manufactured|lots|multi_family | [optional] |
| **sqft_min** | **Integer** |  | [optional] |
| **sqft_max** | **Integer** |  | [optional] |
| **lot_min** | **Integer** |  | [optional] |
| **lot_max** | **Integer** |  | [optional] |
| **year_built_min** | **Integer** |  | [optional] |
| **year_built_max** | **Integer** |  | [optional] |
| **hoa_max** | **Integer** |  | [optional] |
| **keywords** | **String** |  | [optional] |
| **days_on** | **String** |  | [optional] |
| **north** | **Float** | Map bounds for tiling past the 820 cap | [optional] |
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


## zillow_zillow_scraper_health_check

> Object zillow_zillow_scraper_health_check

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::ZillowApi.new

begin
  # Zillow scraper health check
  result = api_instance.zillow_zillow_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_zillow_scraper_health_check: #{e}"
end
```

#### Using the zillow_zillow_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> zillow_zillow_scraper_health_check_with_http_info

```ruby
begin
  # Zillow scraper health check
  data, status_code, headers = api_instance.zillow_zillow_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_zillow_scraper_health_check_with_http_info: #{e}"
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


## zillow_zillow_scraper_health_check_head

> Object zillow_zillow_scraper_health_check_head

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::ZillowApi.new

begin
  # Zillow scraper health check
  result = api_instance.zillow_zillow_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_zillow_scraper_health_check_head: #{e}"
end
```

#### Using the zillow_zillow_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> zillow_zillow_scraper_health_check_head_with_http_info

```ruby
begin
  # Zillow scraper health check
  data, status_code, headers = api_instance.zillow_zillow_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ZillowApi->zillow_zillow_scraper_health_check_head_with_http_info: #{e}"
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

