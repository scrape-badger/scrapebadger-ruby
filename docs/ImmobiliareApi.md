# ScrapeBadger::ImmobiliareApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**immobiliare_get_agency_profile**](ImmobiliareApi.md#immobiliare_get_agency_profile) | **GET** /v1/immobiliare/agencies/{agency_id} | Get agency profile |
| [**immobiliare_get_an_agency_s_listings**](ImmobiliareApi.md#immobiliare_get_an_agency_s_listings) | **GET** /v1/immobiliare/agencies/{agency_id}/listings | Get an agency&#39;s listings |
| [**immobiliare_get_listing_detail**](ImmobiliareApi.md#immobiliare_get_listing_detail) | **GET** /v1/immobiliare/listings/{listing_id} | Get listing detail |
| [**immobiliare_immobiliare_scraper_health_check**](ImmobiliareApi.md#immobiliare_immobiliare_scraper_health_check) | **GET** /v1/immobiliare/health | Immobiliare scraper health check |
| [**immobiliare_immobiliare_scraper_health_check_head**](ImmobiliareApi.md#immobiliare_immobiliare_scraper_health_check_head) | **HEAD** /v1/immobiliare/health | Immobiliare scraper health check |
| [**immobiliare_list_filter_enums**](ImmobiliareApi.md#immobiliare_list_filter_enums) | **GET** /v1/immobiliare/reference | List filter enums |
| [**immobiliare_list_markets**](ImmobiliareApi.md#immobiliare_list_markets) | **GET** /v1/immobiliare/markets | List markets |
| [**immobiliare_location_autocomplete**](ImmobiliareApi.md#immobiliare_location_autocomplete) | **GET** /v1/immobiliare/autocomplete | Location autocomplete |
| [**immobiliare_price_m_time_series**](ImmobiliareApi.md#immobiliare_price_m_time_series) | **GET** /v1/immobiliare/market-insights/prices | Price €/m² time series |
| [**immobiliare_search_listings**](ImmobiliareApi.md#immobiliare_search_listings) | **GET** /v1/immobiliare/search | Search listings |


## immobiliare_get_agency_profile

> Object immobiliare_get_agency_profile(agency_id, opts)

Get agency profile

Public agency/advertiser profile.

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

api_instance = ScrapeBadger::ImmobiliareApi.new
agency_id = 56 # Integer | 
opts = {
  market: 'market_example' # String | it | es | gr | lu
}

begin
  # Get agency profile
  result = api_instance.immobiliare_get_agency_profile(agency_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_get_agency_profile: #{e}"
end
```

#### Using the immobiliare_get_agency_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_get_agency_profile_with_http_info(agency_id, opts)

```ruby
begin
  # Get agency profile
  data, status_code, headers = api_instance.immobiliare_get_agency_profile_with_http_info(agency_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_get_agency_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **agency_id** | **Integer** |  |  |
| **market** | **String** | it | es | gr | lu | [optional][default to &#39;it&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## immobiliare_get_an_agency_s_listings

> Object immobiliare_get_an_agency_s_listings(agency_id, opts)

Get an agency's listings

An agency's active listings.

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

api_instance = ScrapeBadger::ImmobiliareApi.new
agency_id = 56 # Integer | 
opts = {
  market: 'market_example', # String | it | es | gr | lu
  contract: 'contract_example', # String | sale | rent
  page: 56 # Integer | 
}

begin
  # Get an agency's listings
  result = api_instance.immobiliare_get_an_agency_s_listings(agency_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_get_an_agency_s_listings: #{e}"
end
```

#### Using the immobiliare_get_an_agency_s_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_get_an_agency_s_listings_with_http_info(agency_id, opts)

```ruby
begin
  # Get an agency's listings
  data, status_code, headers = api_instance.immobiliare_get_an_agency_s_listings_with_http_info(agency_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_get_an_agency_s_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **agency_id** | **Integer** |  |  |
| **market** | **String** | it | es | gr | lu | [optional][default to &#39;it&#39;] |
| **contract** | **String** | sale | rent | [optional][default to &#39;sale&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## immobiliare_get_listing_detail

> Object immobiliare_get_listing_detail(listing_id, opts)

Get listing detail

Full detail for a single listing.

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

api_instance = ScrapeBadger::ImmobiliareApi.new
listing_id = 56 # Integer | 
opts = {
  market: 'market_example' # String | it | es | gr | lu
}

begin
  # Get listing detail
  result = api_instance.immobiliare_get_listing_detail(listing_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_get_listing_detail: #{e}"
end
```

#### Using the immobiliare_get_listing_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_get_listing_detail_with_http_info(listing_id, opts)

```ruby
begin
  # Get listing detail
  data, status_code, headers = api_instance.immobiliare_get_listing_detail_with_http_info(listing_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_get_listing_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **listing_id** | **Integer** |  |  |
| **market** | **String** | it | es | gr | lu | [optional][default to &#39;it&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## immobiliare_immobiliare_scraper_health_check

> Object immobiliare_immobiliare_scraper_health_check

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::ImmobiliareApi.new

begin
  # Immobiliare scraper health check
  result = api_instance.immobiliare_immobiliare_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_immobiliare_scraper_health_check: #{e}"
end
```

#### Using the immobiliare_immobiliare_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_immobiliare_scraper_health_check_with_http_info

```ruby
begin
  # Immobiliare scraper health check
  data, status_code, headers = api_instance.immobiliare_immobiliare_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_immobiliare_scraper_health_check_with_http_info: #{e}"
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


## immobiliare_immobiliare_scraper_health_check_head

> Object immobiliare_immobiliare_scraper_health_check_head

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::ImmobiliareApi.new

begin
  # Immobiliare scraper health check
  result = api_instance.immobiliare_immobiliare_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_immobiliare_scraper_health_check_head: #{e}"
end
```

#### Using the immobiliare_immobiliare_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_immobiliare_scraper_health_check_head_with_http_info

```ruby
begin
  # Immobiliare scraper health check
  data, status_code, headers = api_instance.immobiliare_immobiliare_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_immobiliare_scraper_health_check_head_with_http_info: #{e}"
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


## immobiliare_list_filter_enums

> Object immobiliare_list_filter_enums

List filter enums

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

api_instance = ScrapeBadger::ImmobiliareApi.new

begin
  # List filter enums
  result = api_instance.immobiliare_list_filter_enums
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_list_filter_enums: #{e}"
end
```

#### Using the immobiliare_list_filter_enums_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_list_filter_enums_with_http_info

```ruby
begin
  # List filter enums
  data, status_code, headers = api_instance.immobiliare_list_filter_enums_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_list_filter_enums_with_http_info: #{e}"
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


## immobiliare_list_markets

> Object immobiliare_list_markets

List markets

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

api_instance = ScrapeBadger::ImmobiliareApi.new

begin
  # List markets
  result = api_instance.immobiliare_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_list_markets: #{e}"
end
```

#### Using the immobiliare_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.immobiliare_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_list_markets_with_http_info: #{e}"
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


## immobiliare_location_autocomplete

> Object immobiliare_location_autocomplete(query, opts)

Location autocomplete

Resolve a place name to region/province/city ids usable in search.

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

api_instance = ScrapeBadger::ImmobiliareApi.new
query = 'query_example' # String | Free-text place name, e.g. 'Milano'
opts = {
  market: 'market_example' # String | it | es | gr | lu
}

begin
  # Location autocomplete
  result = api_instance.immobiliare_location_autocomplete(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_location_autocomplete: #{e}"
end
```

#### Using the immobiliare_location_autocomplete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_location_autocomplete_with_http_info(query, opts)

```ruby
begin
  # Location autocomplete
  data, status_code, headers = api_instance.immobiliare_location_autocomplete_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_location_autocomplete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Free-text place name, e.g. &#39;Milano&#39; |  |
| **market** | **String** | it | es | gr | lu | [optional][default to &#39;it&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## immobiliare_price_m_time_series

> Object immobiliare_price_m_time_series(region_id, opts)

Price €/m² time series

Historical €/m² price statistics for an area.

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

api_instance = ScrapeBadger::ImmobiliareApi.new
region_id = 'region_id_example' # String | Region id, e.g. 'lom'
opts = {
  market: 'market_example', # String | it | es | gr | lu
  province_id: 'province_id_example', # String | Province id, e.g. 'MI'
  city_id: 'city_id_example', # String | City id (idComune)
  contract: 'contract_example' # String | sale | rent
}

begin
  # Price €/m² time series
  result = api_instance.immobiliare_price_m_time_series(region_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_price_m_time_series: #{e}"
end
```

#### Using the immobiliare_price_m_time_series_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_price_m_time_series_with_http_info(region_id, opts)

```ruby
begin
  # Price €/m² time series
  data, status_code, headers = api_instance.immobiliare_price_m_time_series_with_http_info(region_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_price_m_time_series_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **region_id** | **String** | Region id, e.g. &#39;lom&#39; |  |
| **market** | **String** | it | es | gr | lu | [optional][default to &#39;it&#39;] |
| **province_id** | **String** | Province id, e.g. &#39;MI&#39; | [optional] |
| **city_id** | **String** | City id (idComune) | [optional] |
| **contract** | **String** | sale | rent | [optional][default to &#39;sale&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## immobiliare_search_listings

> Object immobiliare_search_listings(opts)

Search listings

Search Immobiliare-group listings (scope by location + contract + filters).

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

api_instance = ScrapeBadger::ImmobiliareApi.new
opts = {
  market: 'market_example', # String | it | es | gr | lu
  location: 'location_example', # String | Free-text place (auto-resolved)
  region_id: 'region_id_example', # String | fkRegione (from /autocomplete)
  province_id: 'province_id_example', # String | idProvincia (from /autocomplete)
  city_id: 'city_id_example', # String | idComune (from /autocomplete)
  contract: 'contract_example', # String | sale | rent
  category: 'category_example', # String | see /reference
  price_min: 56, # Integer | 
  price_max: 56, # Integer | 
  surface_min: 56, # Integer | 
  surface_max: 56, # Integer | 
  rooms_min: 56, # Integer | 
  rooms_max: 56, # Integer | 
  bathrooms_min: 56, # Integer | 
  sort: 'sort_example', # String | see /reference
  page: 56 # Integer | 
}

begin
  # Search listings
  result = api_instance.immobiliare_search_listings(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_search_listings: #{e}"
end
```

#### Using the immobiliare_search_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> immobiliare_search_listings_with_http_info(opts)

```ruby
begin
  # Search listings
  data, status_code, headers = api_instance.immobiliare_search_listings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ImmobiliareApi->immobiliare_search_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** | it | es | gr | lu | [optional][default to &#39;it&#39;] |
| **location** | **String** | Free-text place (auto-resolved) | [optional] |
| **region_id** | **String** | fkRegione (from /autocomplete) | [optional] |
| **province_id** | **String** | idProvincia (from /autocomplete) | [optional] |
| **city_id** | **String** | idComune (from /autocomplete) | [optional] |
| **contract** | **String** | sale | rent | [optional][default to &#39;sale&#39;] |
| **category** | **String** | see /reference | [optional][default to &#39;residential&#39;] |
| **price_min** | **Integer** |  | [optional] |
| **price_max** | **Integer** |  | [optional] |
| **surface_min** | **Integer** |  | [optional] |
| **surface_max** | **Integer** |  | [optional] |
| **rooms_min** | **Integer** |  | [optional] |
| **rooms_max** | **Integer** |  | [optional] |
| **bathrooms_min** | **Integer** |  | [optional] |
| **sort** | **String** | see /reference | [optional][default to &#39;relevance&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

