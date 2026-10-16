# ScrapeBadger::EtsyApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**etsy_get_categories**](EtsyApi.md#etsy_get_categories) | **GET** /v1/etsy/categories | Get categories |
| [**etsy_get_listing_detail**](EtsyApi.md#etsy_get_listing_detail) | **GET** /v1/etsy/listings/{listing_id} | Get listing detail |
| [**etsy_get_listing_reviews**](EtsyApi.md#etsy_get_listing_reviews) | **GET** /v1/etsy/listings/{listing_id}/reviews | Get listing reviews |
| [**etsy_get_search_suggestions**](EtsyApi.md#etsy_get_search_suggestions) | **GET** /v1/etsy/autocomplete | Get search suggestions |
| [**etsy_get_shop_listings**](EtsyApi.md#etsy_get_shop_listings) | **GET** /v1/etsy/shops/{shop_name}/listings | Get shop listings |
| [**etsy_get_shop_profile**](EtsyApi.md#etsy_get_shop_profile) | **GET** /v1/etsy/shops/{shop_name} | Get shop profile |
| [**etsy_get_shop_reviews**](EtsyApi.md#etsy_get_shop_reviews) | **GET** /v1/etsy/shops/{shop_name}/reviews | Get shop reviews |
| [**etsy_search_listings**](EtsyApi.md#etsy_search_listings) | **GET** /v1/etsy/search | Search listings |


## etsy_get_categories

> Object etsy_get_categories(opts)

Get categories

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

api_instance = ScrapeBadger::EtsyApi.new
opts = {
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get categories
  result = api_instance.etsy_get_categories(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_categories: #{e}"
end
```

#### Using the etsy_get_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> etsy_get_categories_with_http_info(opts)

```ruby
begin
  # Get categories
  data, status_code, headers = api_instance.etsy_get_categories_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en-US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## etsy_get_listing_detail

> Object etsy_get_listing_detail(listing_id, opts)

Get listing detail

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

api_instance = ScrapeBadger::EtsyApi.new
listing_id = 'listing_id_example' # String | 
opts = {
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get listing detail
  result = api_instance.etsy_get_listing_detail(listing_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_listing_detail: #{e}"
end
```

#### Using the etsy_get_listing_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> etsy_get_listing_detail_with_http_info(listing_id, opts)

```ruby
begin
  # Get listing detail
  data, status_code, headers = api_instance.etsy_get_listing_detail_with_http_info(listing_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_listing_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **listing_id** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en-US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## etsy_get_listing_reviews

> Object etsy_get_listing_reviews(listing_id, opts)

Get listing reviews

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

api_instance = ScrapeBadger::EtsyApi.new
listing_id = 'listing_id_example' # String | 
opts = {
  page: 56, # Integer | 
  sort: 'Relevancy', # String | 
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get listing reviews
  result = api_instance.etsy_get_listing_reviews(listing_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_listing_reviews: #{e}"
end
```

#### Using the etsy_get_listing_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> etsy_get_listing_reviews_with_http_info(listing_id, opts)

```ruby
begin
  # Get listing reviews
  data, status_code, headers = api_instance.etsy_get_listing_reviews_with_http_info(listing_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_listing_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **listing_id** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **sort** | **String** |  | [optional][default to &#39;Relevancy&#39;] |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en-US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## etsy_get_search_suggestions

> Object etsy_get_search_suggestions(query, opts)

Get search suggestions

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

api_instance = ScrapeBadger::EtsyApi.new
query = 'query_example' # String | 
opts = {
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get search suggestions
  result = api_instance.etsy_get_search_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_search_suggestions: #{e}"
end
```

#### Using the etsy_get_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> etsy_get_search_suggestions_with_http_info(query, opts)

```ruby
begin
  # Get search suggestions
  data, status_code, headers = api_instance.etsy_get_search_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en-US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## etsy_get_shop_listings

> Object etsy_get_shop_listings(shop_name, opts)

Get shop listings

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

api_instance = ScrapeBadger::EtsyApi.new
shop_name = 'shop_name_example' # String | 
opts = {
  page: 56, # Integer | 
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get shop listings
  result = api_instance.etsy_get_shop_listings(shop_name, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_shop_listings: #{e}"
end
```

#### Using the etsy_get_shop_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> etsy_get_shop_listings_with_http_info(shop_name, opts)

```ruby
begin
  # Get shop listings
  data, status_code, headers = api_instance.etsy_get_shop_listings_with_http_info(shop_name, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_shop_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shop_name** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en-US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## etsy_get_shop_profile

> Object etsy_get_shop_profile(shop_name, opts)

Get shop profile

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

api_instance = ScrapeBadger::EtsyApi.new
shop_name = 'shop_name_example' # String | 
opts = {
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get shop profile
  result = api_instance.etsy_get_shop_profile(shop_name, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_shop_profile: #{e}"
end
```

#### Using the etsy_get_shop_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> etsy_get_shop_profile_with_http_info(shop_name, opts)

```ruby
begin
  # Get shop profile
  data, status_code, headers = api_instance.etsy_get_shop_profile_with_http_info(shop_name, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_shop_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shop_name** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en-US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## etsy_get_shop_reviews

> Object etsy_get_shop_reviews(shop_name, opts)

Get shop reviews

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

api_instance = ScrapeBadger::EtsyApi.new
shop_name = 'shop_name_example' # String | 
opts = {
  page: 56, # Integer | 
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get shop reviews
  result = api_instance.etsy_get_shop_reviews(shop_name, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_shop_reviews: #{e}"
end
```

#### Using the etsy_get_shop_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> etsy_get_shop_reviews_with_http_info(shop_name, opts)

```ruby
begin
  # Get shop reviews
  data, status_code, headers = api_instance.etsy_get_shop_reviews_with_http_info(shop_name, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_get_shop_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shop_name** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en-US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## etsy_search_listings

> Object etsy_search_listings(query, opts)

Search listings

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

api_instance = ScrapeBadger::EtsyApi.new
query = 'query_example' # String | 
opts = {
  page: 56, # Integer | 
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example', # String | 
  sort: 'most_relevant', # String | 
  min_price: 8.14, # Float | 
  max_price: 8.14 # Float | 
}

begin
  # Search listings
  result = api_instance.etsy_search_listings(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_search_listings: #{e}"
end
```

#### Using the etsy_search_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> etsy_search_listings_with_http_info(query, opts)

```ruby
begin
  # Search listings
  data, status_code, headers = api_instance.etsy_search_listings_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EtsyApi->etsy_search_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en-US&#39;] |
| **sort** | **String** |  | [optional][default to &#39;most_relevant&#39;] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

