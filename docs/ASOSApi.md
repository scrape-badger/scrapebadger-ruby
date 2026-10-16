# ScrapeBadger::ASOSApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**asos_get_product_detail**](ASOSApi.md#asos_get_product_detail) | **GET** /v1/asos/products/{product_id} | Get product detail |
| [**asos_get_stock_and_prices**](ASOSApi.md#asos_get_stock_and_prices) | **GET** /v1/asos/stock-price | Get stock and prices |
| [**asos_list_categories**](ASOSApi.md#asos_list_categories) | **GET** /v1/asos/categories | List categories |
| [**asos_list_markets**](ASOSApi.md#asos_list_markets) | **GET** /v1/asos/markets | List markets |
| [**asos_list_search_filters**](ASOSApi.md#asos_list_search_filters) | **GET** /v1/asos/filters | List search filters |
| [**asos_search_products**](ASOSApi.md#asos_search_products) | **GET** /v1/asos/search | Search products |
| [**asos_search_suggestions**](ASOSApi.md#asos_search_suggestions) | **GET** /v1/asos/autocomplete | Search suggestions |


## asos_get_product_detail

> <ProductResponse> asos_get_product_detail(product_id, opts)

Get product detail

Product, live per-size stock and price, images, descriptions, reviews and breadcrumbs.

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

api_instance = ScrapeBadger::ASOSApi.new
product_id = 56 # Integer | 
opts = {
  market: 'market_example', # String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
  store: 'store_example', # String | Override store, e.g. COM or US
  country: 'country_example', # String | ISO country override
  currency: 'currency_example', # String | Currency override
  language: 'language_example' # String | Locale override, e.g. en-GB
}

begin
  # Get product detail
  result = api_instance.asos_get_product_detail(product_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_get_product_detail: #{e}"
end
```

#### Using the asos_get_product_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductResponse>, Integer, Hash)> asos_get_product_detail_with_http_info(product_id, opts)

```ruby
begin
  # Get product detail
  data, status_code, headers = api_instance.asos_get_product_detail_with_http_info(product_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_get_product_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **Integer** |  |  |
| **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional][default to &#39;uk&#39;] |
| **store** | **String** | Override store, e.g. COM or US | [optional] |
| **country** | **String** | ISO country override | [optional] |
| **currency** | **String** | Currency override | [optional] |
| **language** | **String** | Locale override, e.g. en-GB | [optional] |

### Return type

[**ProductResponse**](ProductResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## asos_get_stock_and_prices

> <StockResponse> asos_get_stock_and_prices(product_ids, opts)

Get stock and prices

Refresh product and variant stock/prices; reports missing product ids explicitly.

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

api_instance = ScrapeBadger::ASOSApi.new
product_ids = 'product_ids_example' # String | 1–50 comma-separated product ids
opts = {
  market: 'market_example', # String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
  store: 'store_example', # String | Override store, e.g. COM or US
  country: 'country_example', # String | ISO country override
  currency: 'currency_example', # String | Currency override
  language: 'language_example' # String | Locale override, e.g. en-GB
}

begin
  # Get stock and prices
  result = api_instance.asos_get_stock_and_prices(product_ids, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_get_stock_and_prices: #{e}"
end
```

#### Using the asos_get_stock_and_prices_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StockResponse>, Integer, Hash)> asos_get_stock_and_prices_with_http_info(product_ids, opts)

```ruby
begin
  # Get stock and prices
  data, status_code, headers = api_instance.asos_get_stock_and_prices_with_http_info(product_ids, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StockResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_get_stock_and_prices_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_ids** | **String** | 1–50 comma-separated product ids |  |
| **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional][default to &#39;uk&#39;] |
| **store** | **String** | Override store, e.g. COM or US | [optional] |
| **country** | **String** | ISO country override | [optional] |
| **currency** | **String** | Currency override | [optional] |
| **language** | **String** | Locale override, e.g. en-GB | [optional] |

### Return type

[**StockResponse**](StockResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## asos_list_categories

> Object asos_list_categories(opts)

List categories

Full nested navigation with category ids, names, images and links.

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

api_instance = ScrapeBadger::ASOSApi.new
opts = {
  gender: 'men', # String | 
  market: 'market_example', # String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
  store: 'store_example', # String | Override store, e.g. COM or US
  country: 'country_example', # String | ISO country override
  currency: 'currency_example', # String | Currency override
  language: 'language_example' # String | Locale override, e.g. en-GB
}

begin
  # List categories
  result = api_instance.asos_list_categories(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_list_categories: #{e}"
end
```

#### Using the asos_list_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> asos_list_categories_with_http_info(opts)

```ruby
begin
  # List categories
  data, status_code, headers = api_instance.asos_list_categories_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_list_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gender** | **String** |  | [optional][default to &#39;men&#39;] |
| **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional][default to &#39;uk&#39;] |
| **store** | **String** | Override store, e.g. COM or US | [optional] |
| **country** | **String** | ISO country override | [optional] |
| **currency** | **String** | Currency override | [optional] |
| **language** | **String** | Locale override, e.g. en-GB | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## asos_list_markets

> Object asos_list_markets

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

api_instance = ScrapeBadger::ASOSApi.new

begin
  # List markets
  result = api_instance.asos_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_list_markets: #{e}"
end
```

#### Using the asos_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> asos_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.asos_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_list_markets_with_http_info: #{e}"
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


## asos_list_search_filters

> Object asos_list_search_filters(opts)

List search filters

Facet ids, labels, option counts and selections for a query or category.

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

api_instance = ScrapeBadger::ASOSApi.new
opts = {
  query: 'query_example', # String | 
  category_id: 56, # Integer | 
  market: 'market_example', # String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
  store: 'store_example', # String | Override store, e.g. COM or US
  country: 'country_example', # String | ISO country override
  currency: 'currency_example', # String | Currency override
  language: 'language_example' # String | Locale override, e.g. en-GB
}

begin
  # List search filters
  result = api_instance.asos_list_search_filters(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_list_search_filters: #{e}"
end
```

#### Using the asos_list_search_filters_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> asos_list_search_filters_with_http_info(opts)

```ruby
begin
  # List search filters
  data, status_code, headers = api_instance.asos_list_search_filters_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_list_search_filters_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  | [optional] |
| **category_id** | **Integer** |  | [optional] |
| **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional][default to &#39;uk&#39;] |
| **store** | **String** | Override store, e.g. COM or US | [optional] |
| **country** | **String** | ISO country override | [optional] |
| **currency** | **String** | Currency override | [optional] |
| **language** | **String** | Locale override, e.g. en-GB | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## asos_search_products

> <PortalApiRoutersV1AsosSearchResponse> asos_search_products(opts)

Search products

Search by query, category_id, or both. Includes price, images and filter facets.

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

api_instance = ScrapeBadger::ASOSApi.new
opts = {
  query: 'query_example', # String | Keyword, e.g. shoes
  category_id: 56, # Integer | Category id from navigation
  offset: 56, # Integer | 
  limit: 56, # Integer | 
  sort: 'recommended', # String | 
  brand: 'brand_example', # String | Comma-separated brand facet ids
  colour: 'colour_example', # String | Comma-separated colour facet ids
  size: 'size_example', # String | Comma-separated size facet ids
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  market: 'market_example', # String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
  store: 'store_example', # String | Override store, e.g. COM or US
  country: 'country_example', # String | ISO country override
  currency: 'currency_example', # String | Currency override
  language: 'language_example' # String | Locale override, e.g. en-GB
}

begin
  # Search products
  result = api_instance.asos_search_products(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_search_products: #{e}"
end
```

#### Using the asos_search_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PortalApiRoutersV1AsosSearchResponse>, Integer, Hash)> asos_search_products_with_http_info(opts)

```ruby
begin
  # Search products
  data, status_code, headers = api_instance.asos_search_products_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PortalApiRoutersV1AsosSearchResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_search_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Keyword, e.g. shoes | [optional] |
| **category_id** | **Integer** | Category id from navigation | [optional] |
| **offset** | **Integer** |  | [optional][default to 0] |
| **limit** | **Integer** |  | [optional][default to 48] |
| **sort** | **String** |  | [optional][default to &#39;recommended&#39;] |
| **brand** | **String** | Comma-separated brand facet ids | [optional] |
| **colour** | **String** | Comma-separated colour facet ids | [optional] |
| **size** | **String** | Comma-separated size facet ids | [optional] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional][default to &#39;uk&#39;] |
| **store** | **String** | Override store, e.g. COM or US | [optional] |
| **country** | **String** | ISO country override | [optional] |
| **currency** | **String** | Currency override | [optional] |
| **language** | **String** | Locale override, e.g. en-GB | [optional] |

### Return type

[**PortalApiRoutersV1AsosSearchResponse**](PortalApiRoutersV1AsosSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## asos_search_suggestions

> Object asos_search_suggestions(query, opts)

Search suggestions

Search suggestions with result counts.

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

api_instance = ScrapeBadger::ASOSApi.new
query = 'query_example' # String | 
opts = {
  market: 'market_example', # String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
  store: 'store_example', # String | Override store, e.g. COM or US
  country: 'country_example', # String | ISO country override
  currency: 'currency_example', # String | Currency override
  language: 'language_example' # String | Locale override, e.g. en-GB
}

begin
  # Search suggestions
  result = api_instance.asos_search_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_search_suggestions: #{e}"
end
```

#### Using the asos_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> asos_search_suggestions_with_http_info(query, opts)

```ruby
begin
  # Search suggestions
  data, status_code, headers = api_instance.asos_search_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ASOSApi->asos_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional][default to &#39;uk&#39;] |
| **store** | **String** | Override store, e.g. COM or US | [optional] |
| **country** | **String** | ISO country override | [optional] |
| **currency** | **String** | Currency override | [optional] |
| **language** | **String** | Locale override, e.g. en-GB | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

