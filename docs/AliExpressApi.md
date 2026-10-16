# ScrapeBadger::AliExpressApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**aliexpress_get_category_navigation**](AliExpressApi.md#aliexpress_get_category_navigation) | **GET** /v1/aliexpress/categories | Get category navigation |
| [**aliexpress_get_product_detail**](AliExpressApi.md#aliexpress_get_product_detail) | **GET** /v1/aliexpress/products/{product_id} | Get product detail |
| [**aliexpress_get_product_reviews**](AliExpressApi.md#aliexpress_get_product_reviews) | **GET** /v1/aliexpress/products/{product_id}/reviews | Get product reviews |
| [**aliexpress_get_search_suggestions**](AliExpressApi.md#aliexpress_get_search_suggestions) | **GET** /v1/aliexpress/autocomplete | Get search suggestions |
| [**aliexpress_get_store_product_categories**](AliExpressApi.md#aliexpress_get_store_product_categories) | **GET** /v1/aliexpress/stores/{store_id}/categories | Get store product categories |
| [**aliexpress_get_store_products**](AliExpressApi.md#aliexpress_get_store_products) | **GET** /v1/aliexpress/stores/{store_id}/products | Get store products |
| [**aliexpress_get_store_profile**](AliExpressApi.md#aliexpress_get_store_profile) | **GET** /v1/aliexpress/stores/{store_id} | Get store profile |
| [**aliexpress_search_products**](AliExpressApi.md#aliexpress_search_products) | **GET** /v1/aliexpress/search | Search products |


## aliexpress_get_category_navigation

> Object aliexpress_get_category_navigation

Get category navigation

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

api_instance = ScrapeBadger::AliExpressApi.new

begin
  # Get category navigation
  result = api_instance.aliexpress_get_category_navigation
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_category_navigation: #{e}"
end
```

#### Using the aliexpress_get_category_navigation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> aliexpress_get_category_navigation_with_http_info

```ruby
begin
  # Get category navigation
  data, status_code, headers = api_instance.aliexpress_get_category_navigation_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_category_navigation_with_http_info: #{e}"
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


## aliexpress_get_product_detail

> Object aliexpress_get_product_detail(product_id, opts)

Get product detail

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

api_instance = ScrapeBadger::AliExpressApi.new
product_id = 'product_id_example' # String | 
opts = {
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get product detail
  result = api_instance.aliexpress_get_product_detail(product_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_product_detail: #{e}"
end
```

#### Using the aliexpress_get_product_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> aliexpress_get_product_detail_with_http_info(product_id, opts)

```ruby
begin
  # Get product detail
  data, status_code, headers = api_instance.aliexpress_get_product_detail_with_http_info(product_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_product_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en_US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## aliexpress_get_product_reviews

> Object aliexpress_get_product_reviews(product_id, opts)

Get product reviews

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

api_instance = ScrapeBadger::AliExpressApi.new
product_id = 'product_id_example' # String | 
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  sort: 'complex_default' # String | 
}

begin
  # Get product reviews
  result = api_instance.aliexpress_get_product_reviews(product_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_product_reviews: #{e}"
end
```

#### Using the aliexpress_get_product_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> aliexpress_get_product_reviews_with_http_info(product_id, opts)

```ruby
begin
  # Get product reviews
  data, status_code, headers = api_instance.aliexpress_get_product_reviews_with_http_info(product_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_product_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 10] |
| **sort** | **String** |  | [optional][default to &#39;complex_default&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## aliexpress_get_search_suggestions

> Object aliexpress_get_search_suggestions(query, opts)

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

api_instance = ScrapeBadger::AliExpressApi.new
query = 'query_example' # String | 
opts = {
  country: 'country_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get search suggestions
  result = api_instance.aliexpress_get_search_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_search_suggestions: #{e}"
end
```

#### Using the aliexpress_get_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> aliexpress_get_search_suggestions_with_http_info(query, opts)

```ruby
begin
  # Get search suggestions
  data, status_code, headers = api_instance.aliexpress_get_search_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **language** | **String** |  | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## aliexpress_get_store_product_categories

> Object aliexpress_get_store_product_categories(store_id, opts)

Get store product categories

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

api_instance = ScrapeBadger::AliExpressApi.new
store_id = 'store_id_example' # String | 
opts = {
  country: 'country_example' # String | 
}

begin
  # Get store product categories
  result = api_instance.aliexpress_get_store_product_categories(store_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_store_product_categories: #{e}"
end
```

#### Using the aliexpress_get_store_product_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> aliexpress_get_store_product_categories_with_http_info(store_id, opts)

```ruby
begin
  # Get store product categories
  data, status_code, headers = api_instance.aliexpress_get_store_product_categories_with_http_info(store_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_store_product_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **store_id** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## aliexpress_get_store_products

> Object aliexpress_get_store_products(store_id, opts)

Get store products

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

api_instance = ScrapeBadger::AliExpressApi.new
store_id = 'store_id_example' # String | 
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example', # String | 
  query: 'query_example', # String | 
  sort: 'bestmatch_sort' # String | 
}

begin
  # Get store products
  result = api_instance.aliexpress_get_store_products(store_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_store_products: #{e}"
end
```

#### Using the aliexpress_get_store_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> aliexpress_get_store_products_with_http_info(store_id, opts)

```ruby
begin
  # Get store products
  data, status_code, headers = api_instance.aliexpress_get_store_products_with_http_info(store_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_store_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **store_id** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 24] |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en&#39;] |
| **query** | **String** |  | [optional][default to &#39;&#39;] |
| **sort** | **String** |  | [optional][default to &#39;bestmatch_sort&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## aliexpress_get_store_profile

> Object aliexpress_get_store_profile(store_id, opts)

Get store profile

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

api_instance = ScrapeBadger::AliExpressApi.new
store_id = 'store_id_example' # String | 
opts = {
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example' # String | 
}

begin
  # Get store profile
  result = api_instance.aliexpress_get_store_profile(store_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_store_profile: #{e}"
end
```

#### Using the aliexpress_get_store_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> aliexpress_get_store_profile_with_http_info(store_id, opts)

```ruby
begin
  # Get store profile
  data, status_code, headers = api_instance.aliexpress_get_store_profile_with_http_info(store_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_get_store_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **store_id** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## aliexpress_search_products

> Object aliexpress_search_products(query, opts)

Search products

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

api_instance = ScrapeBadger::AliExpressApi.new
query = 'query_example' # String | 
opts = {
  page: 56, # Integer | 
  country: 'country_example', # String | 
  currency: 'currency_example', # String | 
  language: 'language_example', # String | 
  sort: 'default', # String | 
  min_price: 8.14, # Float | 
  max_price: 8.14 # Float | 
}

begin
  # Search products
  result = api_instance.aliexpress_search_products(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_search_products: #{e}"
end
```

#### Using the aliexpress_search_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> aliexpress_search_products_with_http_info(query, opts)

```ruby
begin
  # Search products
  data, status_code, headers = api_instance.aliexpress_search_products_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AliExpressApi->aliexpress_search_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **language** | **String** |  | [optional][default to &#39;en&#39;] |
| **sort** | **String** |  | [optional][default to &#39;default&#39;] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

