# ScrapeBadger::BestBuyApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**bestbuy_browse_a_category**](BestBuyApi.md#bestbuy_browse_a_category) | **GET** /v1/bestbuy/category | Browse a category |
| [**bestbuy_get_categories**](BestBuyApi.md#bestbuy_get_categories) | **GET** /v1/bestbuy/categories | Get categories |
| [**bestbuy_get_laptop_and_computer_deals**](BestBuyApi.md#bestbuy_get_laptop_and_computer_deals) | **GET** /v1/bestbuy/deals | Get laptop and computer deals |
| [**bestbuy_get_product_availability**](BestBuyApi.md#bestbuy_get_product_availability) | **GET** /v1/bestbuy/products/{sku}/availability | Get product availability |
| [**bestbuy_get_product_detail**](BestBuyApi.md#bestbuy_get_product_detail) | **GET** /v1/bestbuy/products/{sku} | Get product detail |
| [**bestbuy_get_product_questions**](BestBuyApi.md#bestbuy_get_product_questions) | **GET** /v1/bestbuy/products/{sku}/questions | Get product questions |
| [**bestbuy_get_product_reviews**](BestBuyApi.md#bestbuy_get_product_reviews) | **GET** /v1/bestbuy/products/{sku}/reviews | Get product reviews |
| [**bestbuy_get_search_suggestions**](BestBuyApi.md#bestbuy_get_search_suggestions) | **GET** /v1/bestbuy/autocomplete | Get search suggestions |
| [**bestbuy_list_supported_markets**](BestBuyApi.md#bestbuy_list_supported_markets) | **GET** /v1/bestbuy/markets | List supported markets |
| [**bestbuy_search_products**](BestBuyApi.md#bestbuy_search_products) | **GET** /v1/bestbuy/search | Search products |


## bestbuy_browse_a_category

> Object bestbuy_browse_a_category(category_id, opts)

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

api_instance = ScrapeBadger::BestBuyApi.new
category_id = 'category_id_example' # String | 
opts = {
  page: 56 # Integer | 
}

begin
  # Browse a category
  result = api_instance.bestbuy_browse_a_category(category_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_browse_a_category: #{e}"
end
```

#### Using the bestbuy_browse_a_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_browse_a_category_with_http_info(category_id, opts)

```ruby
begin
  # Browse a category
  data, status_code, headers = api_instance.bestbuy_browse_a_category_with_http_info(category_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_browse_a_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bestbuy_get_categories

> Object bestbuy_get_categories(opts)

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

api_instance = ScrapeBadger::BestBuyApi.new
opts = {
  query: 'query_example' # String | 
}

begin
  # Get categories
  result = api_instance.bestbuy_get_categories(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_categories: #{e}"
end
```

#### Using the bestbuy_get_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_get_categories_with_http_info(opts)

```ruby
begin
  # Get categories
  data, status_code, headers = api_instance.bestbuy_get_categories_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  | [optional][default to &#39;laptop&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bestbuy_get_laptop_and_computer_deals

> Object bestbuy_get_laptop_and_computer_deals(opts)

Get laptop and computer deals

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

api_instance = ScrapeBadger::BestBuyApi.new
opts = {
  page: 56 # Integer | 
}

begin
  # Get laptop and computer deals
  result = api_instance.bestbuy_get_laptop_and_computer_deals(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_laptop_and_computer_deals: #{e}"
end
```

#### Using the bestbuy_get_laptop_and_computer_deals_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_get_laptop_and_computer_deals_with_http_info(opts)

```ruby
begin
  # Get laptop and computer deals
  data, status_code, headers = api_instance.bestbuy_get_laptop_and_computer_deals_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_laptop_and_computer_deals_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bestbuy_get_product_availability

> Object bestbuy_get_product_availability(sku, zip_code, opts)

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

api_instance = ScrapeBadger::BestBuyApi.new
sku = 'sku_example' # String | 
zip_code = 'zip_code_example' # String | 
opts = {
  store_id: 'store_id_example' # String | 
}

begin
  # Get product availability
  result = api_instance.bestbuy_get_product_availability(sku, zip_code, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_product_availability: #{e}"
end
```

#### Using the bestbuy_get_product_availability_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_get_product_availability_with_http_info(sku, zip_code, opts)

```ruby
begin
  # Get product availability
  data, status_code, headers = api_instance.bestbuy_get_product_availability_with_http_info(sku, zip_code, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_product_availability_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sku** | **String** |  |  |
| **zip_code** | **String** |  |  |
| **store_id** | **String** |  | [optional][default to &#39;7&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bestbuy_get_product_detail

> Object bestbuy_get_product_detail(sku)

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

api_instance = ScrapeBadger::BestBuyApi.new
sku = 'sku_example' # String | 

begin
  # Get product detail
  result = api_instance.bestbuy_get_product_detail(sku)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_product_detail: #{e}"
end
```

#### Using the bestbuy_get_product_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_get_product_detail_with_http_info(sku)

```ruby
begin
  # Get product detail
  data, status_code, headers = api_instance.bestbuy_get_product_detail_with_http_info(sku)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_product_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sku** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bestbuy_get_product_questions

> Object bestbuy_get_product_questions(sku, opts)

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

api_instance = ScrapeBadger::BestBuyApi.new
sku = 'sku_example' # String | 
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  query: 'query_example' # String | 
}

begin
  # Get product questions
  result = api_instance.bestbuy_get_product_questions(sku, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_product_questions: #{e}"
end
```

#### Using the bestbuy_get_product_questions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_get_product_questions_with_http_info(sku, opts)

```ruby
begin
  # Get product questions
  data, status_code, headers = api_instance.bestbuy_get_product_questions_with_http_info(sku, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_product_questions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sku** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 10] |
| **query** | **String** |  | [optional][default to &#39;&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bestbuy_get_product_reviews

> Object bestbuy_get_product_reviews(sku, opts)

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

api_instance = ScrapeBadger::BestBuyApi.new
sku = 'sku_example' # String | 
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  sort: 'MOST_RECENT' # String | 
}

begin
  # Get product reviews
  result = api_instance.bestbuy_get_product_reviews(sku, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_product_reviews: #{e}"
end
```

#### Using the bestbuy_get_product_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_get_product_reviews_with_http_info(sku, opts)

```ruby
begin
  # Get product reviews
  data, status_code, headers = api_instance.bestbuy_get_product_reviews_with_http_info(sku, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_product_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sku** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 10] |
| **sort** | **String** |  | [optional][default to &#39;MOST_RECENT&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bestbuy_get_search_suggestions

> Object bestbuy_get_search_suggestions(query)

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

api_instance = ScrapeBadger::BestBuyApi.new
query = 'query_example' # String | 

begin
  # Get search suggestions
  result = api_instance.bestbuy_get_search_suggestions(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_search_suggestions: #{e}"
end
```

#### Using the bestbuy_get_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_get_search_suggestions_with_http_info(query)

```ruby
begin
  # Get search suggestions
  data, status_code, headers = api_instance.bestbuy_get_search_suggestions_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_get_search_suggestions_with_http_info: #{e}"
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


## bestbuy_list_supported_markets

> Object bestbuy_list_supported_markets

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

api_instance = ScrapeBadger::BestBuyApi.new

begin
  # List supported markets
  result = api_instance.bestbuy_list_supported_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_list_supported_markets: #{e}"
end
```

#### Using the bestbuy_list_supported_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_list_supported_markets_with_http_info

```ruby
begin
  # List supported markets
  data, status_code, headers = api_instance.bestbuy_list_supported_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_list_supported_markets_with_http_info: #{e}"
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


## bestbuy_search_products

> Object bestbuy_search_products(query, opts)

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

api_instance = ScrapeBadger::BestBuyApi.new
query = 'query_example' # String | 
opts = {
  page: 56, # Integer | 
  sort: 'best_match' # String | 
}

begin
  # Search products
  result = api_instance.bestbuy_search_products(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_search_products: #{e}"
end
```

#### Using the bestbuy_search_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bestbuy_search_products_with_http_info(query, opts)

```ruby
begin
  # Search products
  data, status_code, headers = api_instance.bestbuy_search_products_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BestBuyApi->bestbuy_search_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **sort** | **String** |  | [optional][default to &#39;best_match&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

