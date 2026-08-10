# ScrapeBadger::ApartmentsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**apartments_apartments_scraper_health_check**](ApartmentsApi.md#apartments_apartments_scraper_health_check) | **GET** /v1/apartments/health | Apartments scraper health check |
| [**apartments_apartments_scraper_health_check_head**](ApartmentsApi.md#apartments_apartments_scraper_health_check_head) | **HEAD** /v1/apartments/health | Apartments scraper health check |
| [**apartments_get_property_detail_by_slug_id**](ApartmentsApi.md#apartments_get_property_detail_by_slug_id) | **GET** /v1/apartments/properties/{slug}/{property_id} | Get property detail by slug + id |
| [**apartments_get_property_detail_by_url**](ApartmentsApi.md#apartments_get_property_detail_by_url) | **GET** /v1/apartments/property | Get property detail by URL |
| [**apartments_search_rental_listings**](ApartmentsApi.md#apartments_search_rental_listings) | **GET** /v1/apartments/search | Search rental listings |


## apartments_apartments_scraper_health_check

> Object apartments_apartments_scraper_health_check

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::ApartmentsApi.new

begin
  # Apartments scraper health check
  result = api_instance.apartments_apartments_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_apartments_scraper_health_check: #{e}"
end
```

#### Using the apartments_apartments_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> apartments_apartments_scraper_health_check_with_http_info

```ruby
begin
  # Apartments scraper health check
  data, status_code, headers = api_instance.apartments_apartments_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_apartments_scraper_health_check_with_http_info: #{e}"
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


## apartments_apartments_scraper_health_check_head

> Object apartments_apartments_scraper_health_check_head

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::ApartmentsApi.new

begin
  # Apartments scraper health check
  result = api_instance.apartments_apartments_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_apartments_scraper_health_check_head: #{e}"
end
```

#### Using the apartments_apartments_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> apartments_apartments_scraper_health_check_head_with_http_info

```ruby
begin
  # Apartments scraper health check
  data, status_code, headers = api_instance.apartments_apartments_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_apartments_scraper_health_check_head_with_http_info: #{e}"
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


## apartments_get_property_detail_by_slug_id

> Object apartments_get_property_detail_by_slug_id(slug, property_id)

Get property detail by slug + id

Get a property by its SEO slug and 7-character listing id.

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

api_instance = ScrapeBadger::ApartmentsApi.new
slug = 'slug_example' # String | 
property_id = 'property_id_example' # String | 

begin
  # Get property detail by slug + id
  result = api_instance.apartments_get_property_detail_by_slug_id(slug, property_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_get_property_detail_by_slug_id: #{e}"
end
```

#### Using the apartments_get_property_detail_by_slug_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> apartments_get_property_detail_by_slug_id_with_http_info(slug, property_id)

```ruby
begin
  # Get property detail by slug + id
  data, status_code, headers = api_instance.apartments_get_property_detail_by_slug_id_with_http_info(slug, property_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_get_property_detail_by_slug_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **slug** | **String** |  |  |
| **property_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## apartments_get_property_detail_by_url

> Object apartments_get_property_detail_by_url(url)

Get property detail by URL

Get an apartments.com property with full per-unit pricing and availability.

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

api_instance = ScrapeBadger::ApartmentsApi.new
url = 'url_example' # String | Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/

begin
  # Get property detail by URL
  result = api_instance.apartments_get_property_detail_by_url(url)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_get_property_detail_by_url: #{e}"
end
```

#### Using the apartments_get_property_detail_by_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> apartments_get_property_detail_by_url_with_http_info(url)

```ruby
begin
  # Get property detail by URL
  data, status_code, headers = api_instance.apartments_get_property_detail_by_url_with_http_info(url)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_get_property_detail_by_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/ |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## apartments_search_rental_listings

> Object apartments_search_rental_listings(location, opts)

Search rental listings

Search apartments.com for rental properties. 40 cards per page.

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

api_instance = ScrapeBadger::ApartmentsApi.new
location = 'location_example' # String | apartments.com location slug, e.g. 'kansas-city-mo'
opts = {
  page: 56, # Integer | 
  beds: 56, # Integer | 0=studio, 1-4 bedrooms
  min_price: 56, # Integer | 
  max_price: 56 # Integer | 
}

begin
  # Search rental listings
  result = api_instance.apartments_search_rental_listings(location, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_search_rental_listings: #{e}"
end
```

#### Using the apartments_search_rental_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> apartments_search_rental_listings_with_http_info(location, opts)

```ruby
begin
  # Search rental listings
  data, status_code, headers = api_instance.apartments_search_rental_listings_with_http_info(location, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ApartmentsApi->apartments_search_rental_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | apartments.com location slug, e.g. &#39;kansas-city-mo&#39; |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **beds** | **Integer** | 0&#x3D;studio, 1-4 bedrooms | [optional] |
| **min_price** | **Integer** |  | [optional] |
| **max_price** | **Integer** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

