# ScrapeBadger::DepopApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**depop_depop_scraper_health_check**](DepopApi.md#depop_depop_scraper_health_check) | **GET** /v1/depop/health | Depop scraper health check |
| [**depop_depop_scraper_health_check_head**](DepopApi.md#depop_depop_scraper_health_check_head) | **HEAD** /v1/depop/health | Depop scraper health check |
| [**depop_get_a_user_s_products**](DepopApi.md#depop_get_a_user_s_products) | **GET** /v1/depop/users/{username}/products | Get a user&#39;s products |
| [**depop_get_product_detail**](DepopApi.md#depop_get_product_detail) | **GET** /v1/depop/products/{product_id} | Get product detail |
| [**depop_get_shop_user_profile**](DepopApi.md#depop_get_shop_user_profile) | **GET** /v1/depop/users/{username} | Get shop/user profile |
| [**depop_list_markets**](DepopApi.md#depop_list_markets) | **GET** /v1/depop/markets | List markets |
| [**depop_search_depop_products**](DepopApi.md#depop_search_depop_products) | **GET** /v1/depop/search | Search Depop products |


## depop_depop_scraper_health_check

> Object depop_depop_scraper_health_check

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::DepopApi.new

begin
  # Depop scraper health check
  result = api_instance.depop_depop_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_depop_scraper_health_check: #{e}"
end
```

#### Using the depop_depop_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_depop_scraper_health_check_with_http_info

```ruby
begin
  # Depop scraper health check
  data, status_code, headers = api_instance.depop_depop_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_depop_scraper_health_check_with_http_info: #{e}"
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


## depop_depop_scraper_health_check_head

> Object depop_depop_scraper_health_check_head

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::DepopApi.new

begin
  # Depop scraper health check
  result = api_instance.depop_depop_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_depop_scraper_health_check_head: #{e}"
end
```

#### Using the depop_depop_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_depop_scraper_health_check_head_with_http_info

```ruby
begin
  # Depop scraper health check
  data, status_code, headers = api_instance.depop_depop_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_depop_scraper_health_check_head_with_http_info: #{e}"
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


## depop_get_a_user_s_products

> Object depop_get_a_user_s_products(username, opts)

Get a user's products

A user's active listings (cursor-paginated).

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

api_instance = ScrapeBadger::DepopApi.new
username = 'username_example' # String | 
opts = {
  market: 'market_example', # String | Market code
  per_page: 56, # Integer | 
  cursor: 'cursor_example' # String | Pagination cursor
}

begin
  # Get a user's products
  result = api_instance.depop_get_a_user_s_products(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_a_user_s_products: #{e}"
end
```

#### Using the depop_get_a_user_s_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_get_a_user_s_products_with_http_info(username, opts)

```ruby
begin
  # Get a user's products
  data, status_code, headers = api_instance.depop_get_a_user_s_products_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_a_user_s_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **market** | **String** | Market code | [optional][default to &#39;us&#39;] |
| **per_page** | **Integer** |  | [optional][default to 24] |
| **cursor** | **String** | Pagination cursor | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## depop_get_product_detail

> Object depop_get_product_detail(product_id, opts)

Get product detail

Full detail for a single product (by numeric id or slug).

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

api_instance = ScrapeBadger::DepopApi.new
product_id = 'product_id_example' # String | 
opts = {
  market: 'market_example' # String | Market code
}

begin
  # Get product detail
  result = api_instance.depop_get_product_detail(product_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_product_detail: #{e}"
end
```

#### Using the depop_get_product_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_get_product_detail_with_http_info(product_id, opts)

```ruby
begin
  # Get product detail
  data, status_code, headers = api_instance.depop_get_product_detail_with_http_info(product_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_product_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |
| **market** | **String** | Market code | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## depop_get_shop_user_profile

> Object depop_get_shop_user_profile(username, opts)

Get shop/user profile

Public shop/user profile by username.

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

api_instance = ScrapeBadger::DepopApi.new
username = 'username_example' # String | 
opts = {
  market: 'market_example' # String | Market code
}

begin
  # Get shop/user profile
  result = api_instance.depop_get_shop_user_profile(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_shop_user_profile: #{e}"
end
```

#### Using the depop_get_shop_user_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_get_shop_user_profile_with_http_info(username, opts)

```ruby
begin
  # Get shop/user profile
  data, status_code, headers = api_instance.depop_get_shop_user_profile_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_shop_user_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **market** | **String** | Market code | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## depop_list_markets

> Object depop_list_markets

List markets

List supported Depop markets (country + currency).

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

api_instance = ScrapeBadger::DepopApi.new

begin
  # List markets
  result = api_instance.depop_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_list_markets: #{e}"
end
```

#### Using the depop_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.depop_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_list_markets_with_http_info: #{e}"
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


## depop_search_depop_products

> Object depop_search_depop_products(query, opts)

Search Depop products

Search the Depop catalog with filters (cursor-paginated).

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

api_instance = ScrapeBadger::DepopApi.new
query = 'query_example' # String | Search text, e.g. 'nike vintage'
opts = {
  market: 'market_example', # String | Market code (us, gb, au, it, fr, ...)
  per_page: 56, # Integer | Results per page
  cursor: 'cursor_example', # String | Pagination cursor (from previous page)
  price_min: 8.14, # Float | Minimum price
  price_max: 8.14, # Float | Maximum price
  brands: 'brands_example', # String | Comma-separated brand IDs
  categories: 'categories_example', # String | Comma-separated category IDs
  sizes: 'sizes_example', # String | Comma-separated size IDs
  conditions: 'conditions_example', # String | Comma-separated condition slugs (brand_new, used_excellent, ...)
  gender: 'gender_example', # String | male | female
  sort: 'sort_example' # String | relevance | newlyListed | priceAscending | priceDescending
}

begin
  # Search Depop products
  result = api_instance.depop_search_depop_products(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_search_depop_products: #{e}"
end
```

#### Using the depop_search_depop_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_search_depop_products_with_http_info(query, opts)

```ruby
begin
  # Search Depop products
  data, status_code, headers = api_instance.depop_search_depop_products_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_search_depop_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search text, e.g. &#39;nike vintage&#39; |  |
| **market** | **String** | Market code (us, gb, au, it, fr, ...) | [optional][default to &#39;us&#39;] |
| **per_page** | **Integer** | Results per page | [optional][default to 24] |
| **cursor** | **String** | Pagination cursor (from previous page) | [optional] |
| **price_min** | **Float** | Minimum price | [optional] |
| **price_max** | **Float** | Maximum price | [optional] |
| **brands** | **String** | Comma-separated brand IDs | [optional] |
| **categories** | **String** | Comma-separated category IDs | [optional] |
| **sizes** | **String** | Comma-separated size IDs | [optional] |
| **conditions** | **String** | Comma-separated condition slugs (brand_new, used_excellent, ...) | [optional] |
| **gender** | **String** | male | female | [optional] |
| **sort** | **String** | relevance | newlyListed | priceAscending | priceDescending | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

