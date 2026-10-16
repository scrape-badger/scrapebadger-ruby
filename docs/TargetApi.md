# ScrapeBadger::TargetApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**target_browse_a_category**](TargetApi.md#target_browse_a_category) | **GET** /v1/target/category | Browse a category |
| [**target_find_nearby_stores**](TargetApi.md#target_find_nearby_stores) | **GET** /v1/target/stores | Find nearby stores |
| [**target_get_categories**](TargetApi.md#target_get_categories) | **GET** /v1/target/categories | Get categories |
| [**target_get_product_availability**](TargetApi.md#target_get_product_availability) | **GET** /v1/target/products/{tcin}/availability | Get product availability |
| [**target_get_product_detail**](TargetApi.md#target_get_product_detail) | **GET** /v1/target/products/{tcin} | Get product detail |
| [**target_get_product_questions**](TargetApi.md#target_get_product_questions) | **GET** /v1/target/products/{tcin}/questions | Get product questions |
| [**target_get_product_reviews**](TargetApi.md#target_get_product_reviews) | **GET** /v1/target/products/{tcin}/reviews | Get product reviews |
| [**target_get_search_suggestions**](TargetApi.md#target_get_search_suggestions) | **GET** /v1/target/autocomplete | Get search suggestions |
| [**target_get_store_detail**](TargetApi.md#target_get_store_detail) | **GET** /v1/target/stores/{store_id} | Get store detail |
| [**target_list_supported_markets**](TargetApi.md#target_list_supported_markets) | **GET** /v1/target/markets | List supported markets |
| [**target_search_products**](TargetApi.md#target_search_products) | **GET** /v1/target/search | Search products |


## target_browse_a_category

> Object target_browse_a_category(category_id, opts)

Browse a category

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

api_instance = ScrapeBadger::TargetApi.new
category_id = 'category_id_example' # String | 
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  store_id: 'store_id_example', # String | 
  zip_code: 'zip_code_example' # String | 
}

begin
  # Browse a category
  result = api_instance.target_browse_a_category(category_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_browse_a_category: #{e}"
end
```

#### Using the target_browse_a_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_browse_a_category_with_http_info(category_id, opts)

```ruby
begin
  # Browse a category
  data, status_code, headers = api_instance.target_browse_a_category_with_http_info(category_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_browse_a_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 24] |
| **store_id** | **String** |  | [optional][default to &#39;1375&#39;] |
| **zip_code** | **String** |  | [optional][default to &#39;55403&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## target_find_nearby_stores

> Object target_find_nearby_stores(zip_code, opts)

Find nearby stores

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

api_instance = ScrapeBadger::TargetApi.new
zip_code = 'zip_code_example' # String | 
opts = {
  limit: 56 # Integer | 
}

begin
  # Find nearby stores
  result = api_instance.target_find_nearby_stores(zip_code, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_find_nearby_stores: #{e}"
end
```

#### Using the target_find_nearby_stores_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_find_nearby_stores_with_http_info(zip_code, opts)

```ruby
begin
  # Find nearby stores
  data, status_code, headers = api_instance.target_find_nearby_stores_with_http_info(zip_code, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_find_nearby_stores_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **zip_code** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## target_get_categories

> Object target_get_categories(opts)

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

api_instance = ScrapeBadger::TargetApi.new
opts = {
  category_id: 'category_id_example' # String | 
}

begin
  # Get categories
  result = api_instance.target_get_categories(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_categories: #{e}"
end
```

#### Using the target_get_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_get_categories_with_http_info(opts)

```ruby
begin
  # Get categories
  data, status_code, headers = api_instance.target_get_categories_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  | [optional][default to &#39;5xtly&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## target_get_product_availability

> Object target_get_product_availability(tcin, zip_code, opts)

Get product availability

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

api_instance = ScrapeBadger::TargetApi.new
tcin = 'tcin_example' # String | 
zip_code = 'zip_code_example' # String | 
opts = {
  limit: 56 # Integer | 
}

begin
  # Get product availability
  result = api_instance.target_get_product_availability(tcin, zip_code, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_product_availability: #{e}"
end
```

#### Using the target_get_product_availability_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_get_product_availability_with_http_info(tcin, zip_code, opts)

```ruby
begin
  # Get product availability
  data, status_code, headers = api_instance.target_get_product_availability_with_http_info(tcin, zip_code, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_product_availability_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tcin** | **String** |  |  |
| **zip_code** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## target_get_product_detail

> Object target_get_product_detail(tcin, opts)

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

api_instance = ScrapeBadger::TargetApi.new
tcin = 'tcin_example' # String | 
opts = {
  store_id: 'store_id_example', # String | 
  zip_code: 'zip_code_example' # String | 
}

begin
  # Get product detail
  result = api_instance.target_get_product_detail(tcin, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_product_detail: #{e}"
end
```

#### Using the target_get_product_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_get_product_detail_with_http_info(tcin, opts)

```ruby
begin
  # Get product detail
  data, status_code, headers = api_instance.target_get_product_detail_with_http_info(tcin, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_product_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tcin** | **String** |  |  |
| **store_id** | **String** |  | [optional][default to &#39;1375&#39;] |
| **zip_code** | **String** |  | [optional][default to &#39;55403&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## target_get_product_questions

> Object target_get_product_questions(tcin, opts)

Get product questions

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

api_instance = ScrapeBadger::TargetApi.new
tcin = 'tcin_example' # String | 
opts = {
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # Get product questions
  result = api_instance.target_get_product_questions(tcin, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_product_questions: #{e}"
end
```

#### Using the target_get_product_questions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_get_product_questions_with_http_info(tcin, opts)

```ruby
begin
  # Get product questions
  data, status_code, headers = api_instance.target_get_product_questions_with_http_info(tcin, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_product_questions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tcin** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## target_get_product_reviews

> Object target_get_product_reviews(tcin, opts)

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

api_instance = ScrapeBadger::TargetApi.new
tcin = 'tcin_example' # String | 
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  sort: 'most_recent' # String | 
}

begin
  # Get product reviews
  result = api_instance.target_get_product_reviews(tcin, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_product_reviews: #{e}"
end
```

#### Using the target_get_product_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_get_product_reviews_with_http_info(tcin, opts)

```ruby
begin
  # Get product reviews
  data, status_code, headers = api_instance.target_get_product_reviews_with_http_info(tcin, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_product_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tcin** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 10] |
| **sort** | **String** |  | [optional][default to &#39;most_recent&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## target_get_search_suggestions

> Object target_get_search_suggestions(query)

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

api_instance = ScrapeBadger::TargetApi.new
query = 'query_example' # String | 

begin
  # Get search suggestions
  result = api_instance.target_get_search_suggestions(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_search_suggestions: #{e}"
end
```

#### Using the target_get_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_get_search_suggestions_with_http_info(query)

```ruby
begin
  # Get search suggestions
  data, status_code, headers = api_instance.target_get_search_suggestions_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## target_get_store_detail

> Object target_get_store_detail(store_id)

Get store detail

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

api_instance = ScrapeBadger::TargetApi.new
store_id = 'store_id_example' # String | 

begin
  # Get store detail
  result = api_instance.target_get_store_detail(store_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_store_detail: #{e}"
end
```

#### Using the target_get_store_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_get_store_detail_with_http_info(store_id)

```ruby
begin
  # Get store detail
  data, status_code, headers = api_instance.target_get_store_detail_with_http_info(store_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_get_store_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **store_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## target_list_supported_markets

> Object target_list_supported_markets

List supported markets

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

api_instance = ScrapeBadger::TargetApi.new

begin
  # List supported markets
  result = api_instance.target_list_supported_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_list_supported_markets: #{e}"
end
```

#### Using the target_list_supported_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_list_supported_markets_with_http_info

```ruby
begin
  # List supported markets
  data, status_code, headers = api_instance.target_list_supported_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_list_supported_markets_with_http_info: #{e}"
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


## target_search_products

> Object target_search_products(query, opts)

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

api_instance = ScrapeBadger::TargetApi.new
query = 'query_example' # String | 
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  store_id: 'store_id_example', # String | 
  zip_code: 'zip_code_example', # String | 
  sort: 'relevance' # String | 
}

begin
  # Search products
  result = api_instance.target_search_products(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_search_products: #{e}"
end
```

#### Using the target_search_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> target_search_products_with_http_info(query, opts)

```ruby
begin
  # Search products
  data, status_code, headers = api_instance.target_search_products_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TargetApi->target_search_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 24] |
| **store_id** | **String** |  | [optional][default to &#39;1375&#39;] |
| **zip_code** | **String** |  | [optional][default to &#39;55403&#39;] |
| **sort** | **String** |  | [optional][default to &#39;relevance&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

