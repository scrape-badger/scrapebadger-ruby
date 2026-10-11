# ScrapeBadger::WallapopApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**wallapop_autocomplete**](WallapopApi.md#wallapop_autocomplete) | **GET** /v1/wallapop/autocomplete | Autocomplete |
| [**wallapop_get_listing_detail**](WallapopApi.md#wallapop_get_listing_detail) | **GET** /v1/wallapop/items/{item_id} | Get listing detail |
| [**wallapop_get_user_listings**](WallapopApi.md#wallapop_get_user_listings) | **GET** /v1/wallapop/users/{user_id}/items | Get user listings |
| [**wallapop_get_user_profile**](WallapopApi.md#wallapop_get_user_profile) | **GET** /v1/wallapop/users/{user_id} | Get user profile |
| [**wallapop_get_user_reviews**](WallapopApi.md#wallapop_get_user_reviews) | **GET** /v1/wallapop/users/{user_id}/reviews | Get user reviews |
| [**wallapop_list_categories**](WallapopApi.md#wallapop_list_categories) | **GET** /v1/wallapop/categories | List categories |
| [**wallapop_list_filter_options**](WallapopApi.md#wallapop_list_filter_options) | **GET** /v1/wallapop/filters/{filter_id}/options | List filter options |
| [**wallapop_list_markets**](WallapopApi.md#wallapop_list_markets) | **GET** /v1/wallapop/markets | List markets |
| [**wallapop_list_search_filters**](WallapopApi.md#wallapop_list_search_filters) | **GET** /v1/wallapop/filters | List search filters |
| [**wallapop_search_listings**](WallapopApi.md#wallapop_search_listings) | **GET** /v1/wallapop/search | Search listings |
| [**wallapop_wallapop_scraper_health_check**](WallapopApi.md#wallapop_wallapop_scraper_health_check) | **GET** /v1/wallapop/health | Wallapop scraper health check |
| [**wallapop_wallapop_scraper_health_check_head**](WallapopApi.md#wallapop_wallapop_scraper_health_check_head) | **HEAD** /v1/wallapop/health | Wallapop scraper health check |


## wallapop_autocomplete

> Object wallapop_autocomplete(query, opts)

Autocomplete

Wallapop's search-box suggestions for a partial query.

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

api_instance = ScrapeBadger::WallapopApi.new
query = 'query_example' # String | Partial search text, e.g. 'bici'
opts = {
  market: 'market_example' # String | Market: es (Spain), it (Italy), pt (Portugal)
}

begin
  # Autocomplete
  result = api_instance.wallapop_autocomplete(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_autocomplete: #{e}"
end
```

#### Using the wallapop_autocomplete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_autocomplete_with_http_info(query, opts)

```ruby
begin
  # Autocomplete
  data, status_code, headers = api_instance.wallapop_autocomplete_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_autocomplete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial search text, e.g. &#39;bici&#39; |  |
| **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional][default to &#39;es&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## wallapop_get_listing_detail

> Object wallapop_get_listing_detail(item_id, opts)

Get listing detail

Full listing detail by id (e.g. nzxeknm5x562) or listing slug.

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

api_instance = ScrapeBadger::WallapopApi.new
item_id = 'item_id_example' # String | 
opts = {
  market: 'market_example' # String | Market: es (Spain), it (Italy), pt (Portugal)
}

begin
  # Get listing detail
  result = api_instance.wallapop_get_listing_detail(item_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_get_listing_detail: #{e}"
end
```

#### Using the wallapop_get_listing_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_get_listing_detail_with_http_info(item_id, opts)

```ruby
begin
  # Get listing detail
  data, status_code, headers = api_instance.wallapop_get_listing_detail_with_http_info(item_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_get_listing_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **String** |  |  |
| **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional][default to &#39;es&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## wallapop_get_user_listings

> Object wallapop_get_user_listings(user_id, opts)

Get user listings

A seller's live listings, 40 per page.

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

api_instance = ScrapeBadger::WallapopApi.new
user_id = 'user_id_example' # String | 
opts = {
  market: 'market_example', # String | Market: es (Spain), it (Italy), pt (Portugal)
  next_page: 'next_page_example' # String | Cursor from the previous page's next_page
}

begin
  # Get user listings
  result = api_instance.wallapop_get_user_listings(user_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_get_user_listings: #{e}"
end
```

#### Using the wallapop_get_user_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_get_user_listings_with_http_info(user_id, opts)

```ruby
begin
  # Get user listings
  data, status_code, headers = api_instance.wallapop_get_user_listings_with_http_info(user_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_get_user_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |
| **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional][default to &#39;es&#39;] |
| **next_page** | **String** | Cursor from the previous page&#39;s next_page | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## wallapop_get_user_profile

> Object wallapop_get_user_profile(user_id, opts)

Get user profile

Seller profile with ratings, sales counters, response rate and verifications.

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

api_instance = ScrapeBadger::WallapopApi.new
user_id = 'user_id_example' # String | 
opts = {
  market: 'market_example' # String | Market: es (Spain), it (Italy), pt (Portugal)
}

begin
  # Get user profile
  result = api_instance.wallapop_get_user_profile(user_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_get_user_profile: #{e}"
end
```

#### Using the wallapop_get_user_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_get_user_profile_with_http_info(user_id, opts)

```ruby
begin
  # Get user profile
  data, status_code, headers = api_instance.wallapop_get_user_profile_with_http_info(user_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_get_user_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |
| **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional][default to &#39;es&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## wallapop_get_user_reviews

> Object wallapop_get_user_reviews(user_id, opts)

Get user reviews

Reviews a seller received, newest first, 40 per page.

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

api_instance = ScrapeBadger::WallapopApi.new
user_id = 'user_id_example' # String | 
opts = {
  market: 'market_example', # String | Market: es (Spain), it (Italy), pt (Portugal)
  next_page: 'next_page_example' # String | Cursor from the previous page's next_page
}

begin
  # Get user reviews
  result = api_instance.wallapop_get_user_reviews(user_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_get_user_reviews: #{e}"
end
```

#### Using the wallapop_get_user_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_get_user_reviews_with_http_info(user_id, opts)

```ruby
begin
  # Get user reviews
  data, status_code, headers = api_instance.wallapop_get_user_reviews_with_http_info(user_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_get_user_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |
| **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional][default to &#39;es&#39;] |
| **next_page** | **String** | Cursor from the previous page&#39;s next_page | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## wallapop_list_categories

> Object wallapop_list_categories(opts)

List categories

The full category tree; ids are usable as the search category_id.

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

api_instance = ScrapeBadger::WallapopApi.new
opts = {
  market: 'market_example' # String | Market: es (Spain), it (Italy), pt (Portugal)
}

begin
  # List categories
  result = api_instance.wallapop_list_categories(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_list_categories: #{e}"
end
```

#### Using the wallapop_list_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_list_categories_with_http_info(opts)

```ruby
begin
  # List categories
  data, status_code, headers = api_instance.wallapop_list_categories_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_list_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional][default to &#39;es&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## wallapop_list_filter_options

> Object wallapop_list_filter_options(filter_id, opts)

List filter options

Long option lists (e.g. brand, model) for filters flagged options_endpoint.

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

api_instance = ScrapeBadger::WallapopApi.new
filter_id = 'filter_id_example' # String | 
opts = {
  category_id: 56, # Integer | Category to scope options to
  query: 'query_example', # String | Search text to scope options to
  market: 'market_example' # String | Market: es (Spain), it (Italy), pt (Portugal)
}

begin
  # List filter options
  result = api_instance.wallapop_list_filter_options(filter_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_list_filter_options: #{e}"
end
```

#### Using the wallapop_list_filter_options_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_list_filter_options_with_http_info(filter_id, opts)

```ruby
begin
  # List filter options
  data, status_code, headers = api_instance.wallapop_list_filter_options_with_http_info(filter_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_list_filter_options_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **filter_id** | **String** |  |  |
| **category_id** | **Integer** | Category to scope options to | [optional] |
| **query** | **String** | Search text to scope options to | [optional] |
| **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional][default to &#39;es&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## wallapop_list_markets

> Object wallapop_list_markets

List markets

Supported Wallapop markets and their default search location.

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

api_instance = ScrapeBadger::WallapopApi.new

begin
  # List markets
  result = api_instance.wallapop_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_list_markets: #{e}"
end
```

#### Using the wallapop_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.wallapop_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_list_markets_with_http_info: #{e}"
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


## wallapop_list_search_filters

> Object wallapop_list_search_filters(opts)

List search filters

The filters Wallapop offers for a category or query, with option ids.

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

api_instance = ScrapeBadger::WallapopApi.new
opts = {
  category_id: 56, # Integer | Category the filters apply to
  query: 'query_example', # String | Search text the filters apply to
  market: 'market_example' # String | Market: es (Spain), it (Italy), pt (Portugal)
}

begin
  # List search filters
  result = api_instance.wallapop_list_search_filters(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_list_search_filters: #{e}"
end
```

#### Using the wallapop_list_search_filters_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_list_search_filters_with_http_info(opts)

```ruby
begin
  # List search filters
  data, status_code, headers = api_instance.wallapop_list_search_filters_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_list_search_filters_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **Integer** | Category the filters apply to | [optional] |
| **query** | **String** | Search text the filters apply to | [optional] |
| **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional][default to &#39;es&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## wallapop_search_listings

> Object wallapop_search_listings(opts)

Search listings

Search Wallapop listings (40 per page). Needs a query, a category_id, or both.

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

api_instance = ScrapeBadger::WallapopApi.new
opts = {
  query: 'query_example', # String | Search text, e.g. 'iphone 14'
  market: 'market_example', # String | Market: es (Spain), it (Italy), pt (Portugal)
  latitude: 8.14, # Float | Search centre latitude (defaults to the market capital)
  longitude: 8.14, # Float | Search centre longitude
  distance_km: 56, # Integer | Search radius
  category_id: 56, # Integer | Category id from /categories
  min_price: 8.14, # Float | Minimum price (EUR)
  max_price: 8.14, # Float | Maximum price (EUR)
  condition: 'condition_example', # String | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all
  brand: 'brand_example', # String | Brand, e.g. Apple
  model: 'model_example', # String | Model, e.g. iPhone 14
  color: 'color_example', # String | Colour id, e.g. black
  time_filter: 'today', # String | Only listings published within this window
  shippable: true, # Boolean | Only listings that ship
  has_warranty: true, # Boolean | Only listings with a warranty
  refurbished: true, # Boolean | Only refurbished listings
  min_year: 56, # Integer | Cars: earliest model year
  max_year: 56, # Integer | Cars: latest model year
  min_km: 56, # Integer | Cars: minimum mileage
  max_km: 56, # Integer | Cars: maximum mileage
  gearbox: 'manual', # String | Cars
  min_horsepower: 56, # Integer | Cars: minimum power
  max_horsepower: 56, # Integer | Cars: maximum power
  order_by: 'most_relevance', # String | Sort order
  next_page: 'next_page_example' # String | Cursor from the previous page's next_page; other parameters are then ignored
}

begin
  # Search listings
  result = api_instance.wallapop_search_listings(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_search_listings: #{e}"
end
```

#### Using the wallapop_search_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_search_listings_with_http_info(opts)

```ruby
begin
  # Search listings
  data, status_code, headers = api_instance.wallapop_search_listings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_search_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search text, e.g. &#39;iphone 14&#39; | [optional] |
| **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional][default to &#39;es&#39;] |
| **latitude** | **Float** | Search centre latitude (defaults to the market capital) | [optional] |
| **longitude** | **Float** | Search centre longitude | [optional] |
| **distance_km** | **Integer** | Search radius | [optional] |
| **category_id** | **Integer** | Category id from /categories | [optional] |
| **min_price** | **Float** | Minimum price (EUR) | [optional] |
| **max_price** | **Float** | Maximum price (EUR) | [optional] |
| **condition** | **String** | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all | [optional] |
| **brand** | **String** | Brand, e.g. Apple | [optional] |
| **model** | **String** | Model, e.g. iPhone 14 | [optional] |
| **color** | **String** | Colour id, e.g. black | [optional] |
| **time_filter** | **String** | Only listings published within this window | [optional] |
| **shippable** | **Boolean** | Only listings that ship | [optional][default to false] |
| **has_warranty** | **Boolean** | Only listings with a warranty | [optional][default to false] |
| **refurbished** | **Boolean** | Only refurbished listings | [optional][default to false] |
| **min_year** | **Integer** | Cars: earliest model year | [optional] |
| **max_year** | **Integer** | Cars: latest model year | [optional] |
| **min_km** | **Integer** | Cars: minimum mileage | [optional] |
| **max_km** | **Integer** | Cars: maximum mileage | [optional] |
| **gearbox** | **String** | Cars | [optional] |
| **min_horsepower** | **Integer** | Cars: minimum power | [optional] |
| **max_horsepower** | **Integer** | Cars: maximum power | [optional] |
| **order_by** | **String** | Sort order | [optional][default to &#39;most_relevance&#39;] |
| **next_page** | **String** | Cursor from the previous page&#39;s next_page; other parameters are then ignored | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## wallapop_wallapop_scraper_health_check

> Object wallapop_wallapop_scraper_health_check

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::WallapopApi.new

begin
  # Wallapop scraper health check
  result = api_instance.wallapop_wallapop_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_wallapop_scraper_health_check: #{e}"
end
```

#### Using the wallapop_wallapop_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_wallapop_scraper_health_check_with_http_info

```ruby
begin
  # Wallapop scraper health check
  data, status_code, headers = api_instance.wallapop_wallapop_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_wallapop_scraper_health_check_with_http_info: #{e}"
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


## wallapop_wallapop_scraper_health_check_head

> Object wallapop_wallapop_scraper_health_check_head

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::WallapopApi.new

begin
  # Wallapop scraper health check
  result = api_instance.wallapop_wallapop_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_wallapop_scraper_health_check_head: #{e}"
end
```

#### Using the wallapop_wallapop_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> wallapop_wallapop_scraper_health_check_head_with_http_info

```ruby
begin
  # Wallapop scraper health check
  data, status_code, headers = api_instance.wallapop_wallapop_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WallapopApi->wallapop_wallapop_scraper_health_check_head_with_http_info: #{e}"
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

