# ScrapeBadger::IdealistaApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**idealista_agency_by_phone**](IdealistaApi.md#idealista_agency_by_phone) | **GET** /v1/idealista/agency/by-phone/{phone} | Agency by phone |
| [**idealista_agency_profile_listings**](IdealistaApi.md#idealista_agency_profile_listings) | **GET** /v1/idealista/agency/{short_name} | Agency profile + listings |
| [**idealista_get_listing_engagement_stats**](IdealistaApi.md#idealista_get_listing_engagement_stats) | **GET** /v1/idealista/properties/{property_code}/stats | Get listing engagement stats |
| [**idealista_get_property_detail**](IdealistaApi.md#idealista_get_property_detail) | **GET** /v1/idealista/properties/{property_code} | Get property detail |
| [**idealista_idealista_scraper_health_check**](IdealistaApi.md#idealista_idealista_scraper_health_check) | **GET** /v1/idealista/health | Idealista scraper health check |
| [**idealista_idealista_scraper_health_check_head**](IdealistaApi.md#idealista_idealista_scraper_health_check_head) | **HEAD** /v1/idealista/health | Idealista scraper health check |
| [**idealista_list_markets**](IdealistaApi.md#idealista_list_markets) | **GET** /v1/idealista/markets | List markets |
| [**idealista_resolve_locations**](IdealistaApi.md#idealista_resolve_locations) | **GET** /v1/idealista/suggest | Resolve locations |
| [**idealista_search_all_beats_result_cap**](IdealistaApi.md#idealista_search_all_beats_result_cap) | **GET** /v1/idealista/search/all | Search all (beats result cap) |
| [**idealista_search_listings**](IdealistaApi.md#idealista_search_listings) | **GET** /v1/idealista/search | Search listings |


## idealista_agency_by_phone

> Object idealista_agency_by_phone(phone, opts)

Agency by phone

Reverse-lookup the agency behind a contact phone (national number), with its listings.

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

api_instance = ScrapeBadger::IdealistaApi.new
phone = 'phone_example' # String | 
opts = {
  market: 'market_example', # String | es|it|pt
  operation: 'operation_example', # String | sale|rent
  property_type: 'property_type_example', # String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
  page: 56, # Integer | 
  max_items: 56, # Integer | 
  include_listings: true # Boolean | 
}

begin
  # Agency by phone
  result = api_instance.idealista_agency_by_phone(phone, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_agency_by_phone: #{e}"
end
```

#### Using the idealista_agency_by_phone_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_agency_by_phone_with_http_info(phone, opts)

```ruby
begin
  # Agency by phone
  data, status_code, headers = api_instance.idealista_agency_by_phone_with_http_info(phone, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_agency_by_phone_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phone** | **String** |  |  |
| **market** | **String** | es|it|pt | [optional][default to &#39;es&#39;] |
| **operation** | **String** | sale|rent | [optional] |
| **property_type** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **max_items** | **Integer** |  | [optional][default to 30] |
| **include_listings** | **Boolean** |  | [optional][default to true] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## idealista_agency_profile_listings

> Object idealista_agency_profile_listings(short_name, opts)

Agency profile + listings

An agency's microsite profile plus a page of its listings (by URL-slug shortName).

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

api_instance = ScrapeBadger::IdealistaApi.new
short_name = 'short_name_example' # String | 
opts = {
  market: 'market_example', # String | es|it|pt
  operation: 'operation_example', # String | sale|rent
  property_type: 'property_type_example', # String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
  page: 56, # Integer | 
  max_items: 56, # Integer | 
  include_listings: true # Boolean | 
}

begin
  # Agency profile + listings
  result = api_instance.idealista_agency_profile_listings(short_name, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_agency_profile_listings: #{e}"
end
```

#### Using the idealista_agency_profile_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_agency_profile_listings_with_http_info(short_name, opts)

```ruby
begin
  # Agency profile + listings
  data, status_code, headers = api_instance.idealista_agency_profile_listings_with_http_info(short_name, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_agency_profile_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **short_name** | **String** |  |  |
| **market** | **String** | es|it|pt | [optional][default to &#39;es&#39;] |
| **operation** | **String** | sale|rent | [optional] |
| **property_type** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **max_items** | **Integer** |  | [optional][default to 30] |
| **include_listings** | **Boolean** |  | [optional][default to true] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## idealista_get_listing_engagement_stats

> Object idealista_get_listing_engagement_stats(property_code, opts)

Get listing engagement stats

Engagement counters for a listing: views, email contacts, sent-to-friend, favourites.

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

api_instance = ScrapeBadger::IdealistaApi.new
property_code = 'property_code_example' # String | 
opts = {
  market: 'market_example', # String | es|it|pt
  locale: 'locale_example' # String | Language for stat labels
}

begin
  # Get listing engagement stats
  result = api_instance.idealista_get_listing_engagement_stats(property_code, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_get_listing_engagement_stats: #{e}"
end
```

#### Using the idealista_get_listing_engagement_stats_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_get_listing_engagement_stats_with_http_info(property_code, opts)

```ruby
begin
  # Get listing engagement stats
  data, status_code, headers = api_instance.idealista_get_listing_engagement_stats_with_http_info(property_code, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_get_listing_engagement_stats_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **property_code** | **String** |  |  |
| **market** | **String** | es|it|pt | [optional][default to &#39;es&#39;] |
| **locale** | **String** | Language for stat labels | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## idealista_get_property_detail

> Object idealista_get_property_detail(property_code, opts)

Get property detail

Get a single Idealista listing's full detail (energy cert, characteristics, media).

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

api_instance = ScrapeBadger::IdealistaApi.new
property_code = 'property_code_example' # String | 
opts = {
  market: 'market_example', # String | es|it|pt
  locale: 'locale_example' # String | Response language (en, es, it, pt)
}

begin
  # Get property detail
  result = api_instance.idealista_get_property_detail(property_code, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_get_property_detail: #{e}"
end
```

#### Using the idealista_get_property_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_get_property_detail_with_http_info(property_code, opts)

```ruby
begin
  # Get property detail
  data, status_code, headers = api_instance.idealista_get_property_detail_with_http_info(property_code, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_get_property_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **property_code** | **String** |  |  |
| **market** | **String** | es|it|pt | [optional][default to &#39;es&#39;] |
| **locale** | **String** | Response language (en, es, it, pt) | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## idealista_idealista_scraper_health_check

> Object idealista_idealista_scraper_health_check

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::IdealistaApi.new

begin
  # Idealista scraper health check
  result = api_instance.idealista_idealista_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_idealista_scraper_health_check: #{e}"
end
```

#### Using the idealista_idealista_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_idealista_scraper_health_check_with_http_info

```ruby
begin
  # Idealista scraper health check
  data, status_code, headers = api_instance.idealista_idealista_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_idealista_scraper_health_check_with_http_info: #{e}"
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


## idealista_idealista_scraper_health_check_head

> Object idealista_idealista_scraper_health_check_head

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::IdealistaApi.new

begin
  # Idealista scraper health check
  result = api_instance.idealista_idealista_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_idealista_scraper_health_check_head: #{e}"
end
```

#### Using the idealista_idealista_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_idealista_scraper_health_check_head_with_http_info

```ruby
begin
  # Idealista scraper health check
  data, status_code, headers = api_instance.idealista_idealista_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_idealista_scraper_health_check_head_with_http_info: #{e}"
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


## idealista_list_markets

> Object idealista_list_markets

List markets

List supported Idealista markets (ES, IT, PT).

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

api_instance = ScrapeBadger::IdealistaApi.new

begin
  # List markets
  result = api_instance.idealista_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_list_markets: #{e}"
end
```

#### Using the idealista_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.idealista_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_list_markets_with_http_info: #{e}"
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


## idealista_resolve_locations

> Object idealista_resolve_locations(query, opts)

Resolve locations

Resolve a free-text query into Idealista location codes for a search.

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

api_instance = ScrapeBadger::IdealistaApi.new
query = 'query_example' # String | Free-text location, e.g. 'sagrada familia'
opts = {
  operation: 'operation_example', # String | sale|rent
  property_type: 'property_type_example', # String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
  market: 'market_example', # String | es|it|pt
  locale: 'locale_example' # String | Response language (en, es, it, pt)
}

begin
  # Resolve locations
  result = api_instance.idealista_resolve_locations(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_resolve_locations: #{e}"
end
```

#### Using the idealista_resolve_locations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_resolve_locations_with_http_info(query, opts)

```ruby
begin
  # Resolve locations
  data, status_code, headers = api_instance.idealista_resolve_locations_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_resolve_locations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Free-text location, e.g. &#39;sagrada familia&#39; |  |
| **operation** | **String** | sale|rent | [optional][default to &#39;sale&#39;] |
| **property_type** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional][default to &#39;homes&#39;] |
| **market** | **String** | es|it|pt | [optional][default to &#39;es&#39;] |
| **locale** | **String** | Response language (en, es, it, pt) | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## idealista_search_all_beats_result_cap

> Object idealista_search_all_beats_result_cap(location, opts)

Search all (beats result cap)

Full inventory for a location, beating Idealista's ~1800 per-search cap via price-range tiling (deduped). Billed per page fetched.

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

api_instance = ScrapeBadger::IdealistaApi.new
location = 'location_example' # String | Idealista location code (from /suggest)
opts = {
  operation: 'operation_example', # String | sale|rent
  property_type: 'property_type_example', # String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
  market: 'market_example', # String | es|it|pt
  max_results: 56, # Integer | 
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  min_size: 8.14, # Float | 
  max_size: 8.14, # Float | 
  min_rooms: 56, # Integer | 
  max_rooms: 56, # Integer | 
  locale: 'locale_example' # String | Response language (en, es, it, pt)
}

begin
  # Search all (beats result cap)
  result = api_instance.idealista_search_all_beats_result_cap(location, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_search_all_beats_result_cap: #{e}"
end
```

#### Using the idealista_search_all_beats_result_cap_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_search_all_beats_result_cap_with_http_info(location, opts)

```ruby
begin
  # Search all (beats result cap)
  data, status_code, headers = api_instance.idealista_search_all_beats_result_cap_with_http_info(location, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_search_all_beats_result_cap_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | Idealista location code (from /suggest) |  |
| **operation** | **String** | sale|rent | [optional][default to &#39;sale&#39;] |
| **property_type** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional][default to &#39;homes&#39;] |
| **market** | **String** | es|it|pt | [optional][default to &#39;es&#39;] |
| **max_results** | **Integer** |  | [optional][default to 500] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **min_size** | **Float** |  | [optional] |
| **max_size** | **Float** |  | [optional] |
| **min_rooms** | **Integer** |  | [optional] |
| **max_rooms** | **Integer** |  | [optional] |
| **locale** | **String** | Response language (en, es, it, pt) | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## idealista_search_listings

> Object idealista_search_listings(location, opts)

Search listings

Search Idealista real-estate listings by location code.

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

api_instance = ScrapeBadger::IdealistaApi.new
location = 'location_example' # String | Idealista location code (from /suggest)
opts = {
  operation: 'operation_example', # String | sale|rent
  property_type: 'property_type_example', # String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
  market: 'market_example', # String | es|it|pt
  page: 56, # Integer | 
  max_items: 56, # Integer | 
  sort_by: 'sort_by_example', # String | distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds
  sort_order: 'sort_order_example', # String | asc|desc
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  min_size: 8.14, # Float | 
  max_size: 8.14, # Float | 
  min_rooms: 56, # Integer | 
  max_rooms: 56, # Integer | 
  locale: 'locale_example' # String | Response language (en, es, it, pt)
}

begin
  # Search listings
  result = api_instance.idealista_search_listings(location, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_search_listings: #{e}"
end
```

#### Using the idealista_search_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> idealista_search_listings_with_http_info(location, opts)

```ruby
begin
  # Search listings
  data, status_code, headers = api_instance.idealista_search_listings_with_http_info(location, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling IdealistaApi->idealista_search_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | Idealista location code (from /suggest) |  |
| **operation** | **String** | sale|rent | [optional][default to &#39;sale&#39;] |
| **property_type** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional][default to &#39;homes&#39;] |
| **market** | **String** | es|it|pt | [optional][default to &#39;es&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **max_items** | **Integer** |  | [optional][default to 30] |
| **sort_by** | **String** | distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds | [optional] |
| **sort_order** | **String** | asc|desc | [optional][default to &#39;desc&#39;] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **min_size** | **Float** |  | [optional] |
| **max_size** | **Float** |  | [optional] |
| **min_rooms** | **Integer** |  | [optional] |
| **max_rooms** | **Integer** |  | [optional] |
| **locale** | **String** | Response language (en, es, it, pt) | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

