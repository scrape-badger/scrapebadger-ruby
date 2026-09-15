# ScrapeBadger::VintedApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**vinted_get_item_details**](VintedApi.md#vinted_get_item_details) | **GET** /v1/vinted/items/{item_id} | Get item details |
| [**vinted_get_user_profile**](VintedApi.md#vinted_get_user_profile) | **GET** /v1/vinted/users/{user_id} | Get user profile |
| [**vinted_get_user_s_listed_items**](VintedApi.md#vinted_get_user_s_listed_items) | **GET** /v1/vinted/users/{user_id}/items | Get user&#39;s listed items |
| [**vinted_list_colors**](VintedApi.md#vinted_list_colors) | **GET** /v1/vinted/colors | List colors |
| [**vinted_list_item_conditions**](VintedApi.md#vinted_list_item_conditions) | **GET** /v1/vinted/statuses | List item conditions |
| [**vinted_list_markets**](VintedApi.md#vinted_list_markets) | **GET** /v1/vinted/markets | List markets |
| [**vinted_list_public_vinted_mobile_operations**](VintedApi.md#vinted_list_public_vinted_mobile_operations) | **GET** /v1/vinted/mobile/operations | List public Vinted mobile operations |
| [**vinted_read_vinted_mobile_data**](VintedApi.md#vinted_read_vinted_mobile_data) | **POST** /v1/vinted/mobile/{operation} | Read Vinted mobile data |
| [**vinted_search_brands**](VintedApi.md#vinted_search_brands) | **GET** /v1/vinted/brands | Search brands |
| [**vinted_search_by_image**](VintedApi.md#vinted_search_by_image) | **POST** /v1/vinted/search_by_image | Search by image |
| [**vinted_search_vinted_items**](VintedApi.md#vinted_search_vinted_items) | **GET** /v1/vinted/search | Search Vinted items |
| [**vinted_vinted_scraper_health_check**](VintedApi.md#vinted_vinted_scraper_health_check) | **GET** /v1/vinted/health | Vinted scraper health check |
| [**vinted_vinted_scraper_health_check_head**](VintedApi.md#vinted_vinted_scraper_health_check_head) | **HEAD** /v1/vinted/health | Vinted scraper health check |


## vinted_get_item_details

> Object vinted_get_item_details(item_id, opts)

Get item details

Get detailed information about a Vinted item.

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

api_instance = ScrapeBadger::VintedApi.new
item_id = 56 # Integer | 
opts = {
  market: 'market_example' # String | 
}

begin
  # Get item details
  result = api_instance.vinted_get_item_details(item_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_get_item_details: #{e}"
end
```

#### Using the vinted_get_item_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_get_item_details_with_http_info(item_id, opts)

```ruby
begin
  # Get item details
  data, status_code, headers = api_instance.vinted_get_item_details_with_http_info(item_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_get_item_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **Integer** |  |  |
| **market** | **String** |  | [optional][default to &#39;fr&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## vinted_get_user_profile

> Object vinted_get_user_profile(user_id, opts)

Get user profile

Get a Vinted user's profile.

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

api_instance = ScrapeBadger::VintedApi.new
user_id = 56 # Integer | 
opts = {
  market: 'market_example' # String | 
}

begin
  # Get user profile
  result = api_instance.vinted_get_user_profile(user_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_get_user_profile: #{e}"
end
```

#### Using the vinted_get_user_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_get_user_profile_with_http_info(user_id, opts)

```ruby
begin
  # Get user profile
  data, status_code, headers = api_instance.vinted_get_user_profile_with_http_info(user_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_get_user_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **Integer** |  |  |
| **market** | **String** |  | [optional][default to &#39;fr&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## vinted_get_user_s_listed_items

> Object vinted_get_user_s_listed_items(user_id, opts)

Get user's listed items

Get items listed by a Vinted user.

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

api_instance = ScrapeBadger::VintedApi.new
user_id = 56 # Integer | 
opts = {
  market: 'market_example', # String | 
  page: 56, # Integer | 
  per_page: 56 # Integer | 
}

begin
  # Get user's listed items
  result = api_instance.vinted_get_user_s_listed_items(user_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_get_user_s_listed_items: #{e}"
end
```

#### Using the vinted_get_user_s_listed_items_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_get_user_s_listed_items_with_http_info(user_id, opts)

```ruby
begin
  # Get user's listed items
  data, status_code, headers = api_instance.vinted_get_user_s_listed_items_with_http_info(user_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_get_user_s_listed_items_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **Integer** |  |  |
| **market** | **String** |  | [optional][default to &#39;fr&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** |  | [optional][default to 20] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## vinted_list_colors

> Object vinted_list_colors(opts)

List colors

Get available Vinted colors for filtering.

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

api_instance = ScrapeBadger::VintedApi.new
opts = {
  market: 'market_example' # String | 
}

begin
  # List colors
  result = api_instance.vinted_list_colors(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_list_colors: #{e}"
end
```

#### Using the vinted_list_colors_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_list_colors_with_http_info(opts)

```ruby
begin
  # List colors
  data, status_code, headers = api_instance.vinted_list_colors_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_list_colors_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** |  | [optional][default to &#39;fr&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## vinted_list_item_conditions

> Object vinted_list_item_conditions(opts)

List item conditions

Get available item condition statuses.

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

api_instance = ScrapeBadger::VintedApi.new
opts = {
  market: 'market_example' # String | 
}

begin
  # List item conditions
  result = api_instance.vinted_list_item_conditions(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_list_item_conditions: #{e}"
end
```

#### Using the vinted_list_item_conditions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_list_item_conditions_with_http_info(opts)

```ruby
begin
  # List item conditions
  data, status_code, headers = api_instance.vinted_list_item_conditions_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_list_item_conditions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** |  | [optional][default to &#39;fr&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## vinted_list_markets

> Object vinted_list_markets

List markets

List all supported Vinted markets.

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

api_instance = ScrapeBadger::VintedApi.new

begin
  # List markets
  result = api_instance.vinted_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_list_markets: #{e}"
end
```

#### Using the vinted_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.vinted_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_list_markets_with_http_info: #{e}"
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


## vinted_list_public_vinted_mobile_operations

> Object vinted_list_public_vinted_mobile_operations

List public Vinted mobile operations

Discover public read operations, parameters and runnable examples. Free.

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

api_instance = ScrapeBadger::VintedApi.new

begin
  # List public Vinted mobile operations
  result = api_instance.vinted_list_public_vinted_mobile_operations
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_list_public_vinted_mobile_operations: #{e}"
end
```

#### Using the vinted_list_public_vinted_mobile_operations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_list_public_vinted_mobile_operations_with_http_info

```ruby
begin
  # List public Vinted mobile operations
  data, status_code, headers = api_instance.vinted_list_public_vinted_mobile_operations_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_list_public_vinted_mobile_operations_with_http_info: #{e}"
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


## vinted_read_vinted_mobile_data

> Object vinted_read_vinted_mobile_data(operation, vinted_mobile_read_request)

Read Vinted mobile data

Read catalog, listing, seller, review, sold-comparable, pricing, reference, shipping-reference, homepage or help data. No Vinted account is required. This is an allowlisted read API, including read-only upstream POST queries. Returns operation, market, and the upstream JSON under data. One credit. Sold comparable prices are not guaranteed final negotiated sale prices.

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

api_instance = ScrapeBadger::VintedApi.new
operation = 'operation_example' # String | 
vinted_mobile_read_request = ScrapeBadger::VintedMobileReadRequest.new # VintedMobileReadRequest | 

begin
  # Read Vinted mobile data
  result = api_instance.vinted_read_vinted_mobile_data(operation, vinted_mobile_read_request)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_read_vinted_mobile_data: #{e}"
end
```

#### Using the vinted_read_vinted_mobile_data_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_read_vinted_mobile_data_with_http_info(operation, vinted_mobile_read_request)

```ruby
begin
  # Read Vinted mobile data
  data, status_code, headers = api_instance.vinted_read_vinted_mobile_data_with_http_info(operation, vinted_mobile_read_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_read_vinted_mobile_data_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **operation** | **String** |  |  |
| **vinted_mobile_read_request** | [**VintedMobileReadRequest**](VintedMobileReadRequest.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## vinted_search_brands

> Object vinted_search_brands(keyword, opts)

Search brands

Search Vinted brands.

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

api_instance = ScrapeBadger::VintedApi.new
keyword = 'keyword_example' # String | Brand search keyword
opts = {
  market: 'market_example' # String | 
}

begin
  # Search brands
  result = api_instance.vinted_search_brands(keyword, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_search_brands: #{e}"
end
```

#### Using the vinted_search_brands_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_search_brands_with_http_info(keyword, opts)

```ruby
begin
  # Search brands
  data, status_code, headers = api_instance.vinted_search_brands_with_http_info(keyword, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_search_brands_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **keyword** | **String** | Brand search keyword |  |
| **market** | **String** |  | [optional][default to &#39;fr&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## vinted_search_by_image

> Object vinted_search_by_image(vinted_image_search_request)

Search by image

Find active Vinted listings from a photo. 10 credits per successful request. Returns the usual items, pagination and market envelope. Visual ranking; no similarity score. Resend the same image and pagination time for subsequent pages. Structured brand data may be null.

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

api_instance = ScrapeBadger::VintedApi.new
vinted_image_search_request = ScrapeBadger::VintedImageSearchRequest.new # VintedImageSearchRequest | 

begin
  # Search by image
  result = api_instance.vinted_search_by_image(vinted_image_search_request)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_search_by_image: #{e}"
end
```

#### Using the vinted_search_by_image_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_search_by_image_with_http_info(vinted_image_search_request)

```ruby
begin
  # Search by image
  data, status_code, headers = api_instance.vinted_search_by_image_with_http_info(vinted_image_search_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_search_by_image_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **vinted_image_search_request** | [**VintedImageSearchRequest**](VintedImageSearchRequest.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## vinted_search_vinted_items

> Object vinted_search_vinted_items(query, opts)

Search Vinted items

Search Vinted catalog items with filters.

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

api_instance = ScrapeBadger::VintedApi.new
query = 'query_example' # String | Search text
opts = {
  market: 'market_example', # String | Market code
  seller_country: 'seller_country_example', # String | Filter to items whose seller is physically located in one of these comma-separated ISO-2 country codes (e.g. 'fr' or 'fr,be'). Market domains federate cross-border EU listings and Vinted has no native country filter, so each item is enriched with its seller's country and non-matching ones are dropped. Adds 1 credit per uncached seller looked up (cached for 7 days).
  page: 56, # Integer | 
  per_page: 56, # Integer | 
  price_from: 8.14, # Float | 
  price_to: 8.14, # Float | 
  brand_ids: 'brand_ids_example', # String | 
  catalog_ids: 'catalog_ids_example', # String | Comma-separated Vinted catalog (category) IDs to restrict the search to, e.g. '1904' or '1904,79'. Vinted applies this before searching, so pagination totals reflect the filtered set. A catalog ID is the `catalog[]` value in a Vinted category URL (vinted.fr/catalog?catalog[]=1904).
  color_ids: 'color_ids_example', # String | Comma-separated color IDs
  size_ids: 'size_ids_example', # String | Comma-separated size IDs
  material_ids: 'material_ids_example', # String | Comma-separated material IDs
  time: 56, # Integer | Pagination time returned by the preceding page
  search_session_id: 'search_session_id_example', # String | Reuse across pages of one search
  status_ids: 'status_ids_example', # String | Comma-separated condition/status IDs
  order: 'order_example' # String | 
}

begin
  # Search Vinted items
  result = api_instance.vinted_search_vinted_items(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_search_vinted_items: #{e}"
end
```

#### Using the vinted_search_vinted_items_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_search_vinted_items_with_http_info(query, opts)

```ruby
begin
  # Search Vinted items
  data, status_code, headers = api_instance.vinted_search_vinted_items_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_search_vinted_items_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search text |  |
| **market** | **String** | Market code | [optional][default to &#39;fr&#39;] |
| **seller_country** | **String** | Filter to items whose seller is physically located in one of these comma-separated ISO-2 country codes (e.g. &#39;fr&#39; or &#39;fr,be&#39;). Market domains federate cross-border EU listings and Vinted has no native country filter, so each item is enriched with its seller&#39;s country and non-matching ones are dropped. Adds 1 credit per uncached seller looked up (cached for 7 days). | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** |  | [optional][default to 20] |
| **price_from** | **Float** |  | [optional] |
| **price_to** | **Float** |  | [optional] |
| **brand_ids** | **String** |  | [optional] |
| **catalog_ids** | **String** | Comma-separated Vinted catalog (category) IDs to restrict the search to, e.g. &#39;1904&#39; or &#39;1904,79&#39;. Vinted applies this before searching, so pagination totals reflect the filtered set. A catalog ID is the &#x60;catalog[]&#x60; value in a Vinted category URL (vinted.fr/catalog?catalog[]&#x3D;1904). | [optional] |
| **color_ids** | **String** | Comma-separated color IDs | [optional] |
| **size_ids** | **String** | Comma-separated size IDs | [optional] |
| **material_ids** | **String** | Comma-separated material IDs | [optional] |
| **time** | **Integer** | Pagination time returned by the preceding page | [optional] |
| **search_session_id** | **String** | Reuse across pages of one search | [optional] |
| **status_ids** | **String** | Comma-separated condition/status IDs | [optional] |
| **order** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## vinted_vinted_scraper_health_check

> Object vinted_vinted_scraper_health_check

Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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

api_instance = ScrapeBadger::VintedApi.new

begin
  # Vinted scraper health check
  result = api_instance.vinted_vinted_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_vinted_scraper_health_check: #{e}"
end
```

#### Using the vinted_vinted_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_vinted_scraper_health_check_with_http_info

```ruby
begin
  # Vinted scraper health check
  data, status_code, headers = api_instance.vinted_vinted_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_vinted_scraper_health_check_with_http_info: #{e}"
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


## vinted_vinted_scraper_health_check_head

> Object vinted_vinted_scraper_health_check_head

Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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

api_instance = ScrapeBadger::VintedApi.new

begin
  # Vinted scraper health check
  result = api_instance.vinted_vinted_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_vinted_scraper_health_check_head: #{e}"
end
```

#### Using the vinted_vinted_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> vinted_vinted_scraper_health_check_head_with_http_info

```ruby
begin
  # Vinted scraper health check
  data, status_code, headers = api_instance.vinted_vinted_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling VintedApi->vinted_vinted_scraper_health_check_head_with_http_info: #{e}"
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

