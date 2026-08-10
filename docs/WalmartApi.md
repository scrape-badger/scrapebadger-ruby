# ScrapeBadger::WalmartApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**walmart_browse_a_category**](WalmartApi.md#walmart_browse_a_category) | **GET** /v1/walmart/category | Browse a category |
| [**walmart_deals_rollbacks_and_clearance**](WalmartApi.md#walmart_deals_rollbacks_and_clearance) | **GET** /v1/walmart/deals | Deals, rollbacks and clearance |
| [**walmart_get_a_seller_s_catalogue**](WalmartApi.md#walmart_get_a_seller_s_catalogue) | **GET** /v1/walmart/sellers/{seller_id}/products | Get a seller&#39;s catalogue |
| [**walmart_get_product_detail**](WalmartApi.md#walmart_get_product_detail) | **GET** /v1/walmart/products/{item_id} | Get product detail |
| [**walmart_get_product_reviews**](WalmartApi.md#walmart_get_product_reviews) | **GET** /v1/walmart/products/{item_id}/reviews | Get product reviews |
| [**walmart_get_seller_profile**](WalmartApi.md#walmart_get_seller_profile) | **GET** /v1/walmart/sellers/{seller_id} | Get seller profile |
| [**walmart_get_store_nearby_stores**](WalmartApi.md#walmart_get_store_nearby_stores) | **GET** /v1/walmart/stores/{store_id} | Get store + nearby stores |
| [**walmart_list_supported_markets**](WalmartApi.md#walmart_list_supported_markets) | **GET** /v1/walmart/markets | List supported markets |
| [**walmart_search_products**](WalmartApi.md#walmart_search_products) | **GET** /v1/walmart/search | Search products |
| [**walmart_search_suggestions**](WalmartApi.md#walmart_search_suggestions) | **GET** /v1/walmart/autocomplete | Search suggestions |
| [**walmart_walmart_scraper_health_check**](WalmartApi.md#walmart_walmart_scraper_health_check) | **GET** /v1/walmart/health | Walmart scraper health check |
| [**walmart_walmart_scraper_health_check_head**](WalmartApi.md#walmart_walmart_scraper_health_check_head) | **HEAD** /v1/walmart/health | Walmart scraper health check |


## walmart_browse_a_category

> Object walmart_browse_a_category(path, opts)

Browse a category

Browse a Walmart category. Same result shape as search.  No `sort`: Walmart's browse pages ignore it. Sort on `/search` instead.

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

api_instance = ScrapeBadger::WalmartApi.new
path = 'path_example' # String | Browse path, e.g. 'electronics/3944', or a '/cp/...' path
opts = {
  page: 56, # Integer | 
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  facet: 'facet_example' # String | 
}

begin
  # Browse a category
  result = api_instance.walmart_browse_a_category(path, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_browse_a_category: #{e}"
end
```

#### Using the walmart_browse_a_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_browse_a_category_with_http_info(path, opts)

```ruby
begin
  # Browse a category
  data, status_code, headers = api_instance.walmart_browse_a_category_with_http_info(path, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_browse_a_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **path** | **String** | Browse path, e.g. &#39;electronics/3944&#39;, or a &#39;/cp/...&#39; path |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **facet** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## walmart_deals_rollbacks_and_clearance

> Object walmart_deals_rollbacks_and_clearance(opts)

Deals, rollbacks and clearance

Walmart's current deals, rollbacks and clearance.

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

api_instance = ScrapeBadger::WalmartApi.new
opts = {
  page: 56, # Integer | 
  min_price: 8.14, # Float | 
  max_price: 8.14 # Float | 
}

begin
  # Deals, rollbacks and clearance
  result = api_instance.walmart_deals_rollbacks_and_clearance(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_deals_rollbacks_and_clearance: #{e}"
end
```

#### Using the walmart_deals_rollbacks_and_clearance_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_deals_rollbacks_and_clearance_with_http_info(opts)

```ruby
begin
  # Deals, rollbacks and clearance
  data, status_code, headers = api_instance.walmart_deals_rollbacks_and_clearance_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_deals_rollbacks_and_clearance_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional][default to 1] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## walmart_get_a_seller_s_catalogue

> Object walmart_get_a_seller_s_catalogue(seller_id, query, opts)

Get a seller's catalogue

A marketplace seller's catalogue, scoped by a search term.

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

api_instance = ScrapeBadger::WalmartApi.new
seller_id = 'seller_id_example' # String | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).
query = 'query_example' # String | Required — Walmart returns nothing for a seller facet alone
opts = {
  page: 56, # Integer | 
  sort: 'sort_example' # String | 
}

begin
  # Get a seller's catalogue
  result = api_instance.walmart_get_a_seller_s_catalogue(seller_id, query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_a_seller_s_catalogue: #{e}"
end
```

#### Using the walmart_get_a_seller_s_catalogue_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_get_a_seller_s_catalogue_with_http_info(seller_id, query, opts)

```ruby
begin
  # Get a seller's catalogue
  data, status_code, headers = api_instance.walmart_get_a_seller_s_catalogue_with_http_info(seller_id, query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_a_seller_s_catalogue_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **seller_id** | **String** | Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). |  |
| **query** | **String** | Required — Walmart returns nothing for a seller facet alone |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **sort** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## walmart_get_product_detail

> Object walmart_get_product_detail(item_id)

Get product detail

Full product detail — price, stock, specs, variants, seller, reviews sample.

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

api_instance = ScrapeBadger::WalmartApi.new
item_id = 'item_id_example' # String | Walmart usItemId, e.g. '5689919121'

begin
  # Get product detail
  result = api_instance.walmart_get_product_detail(item_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_product_detail: #{e}"
end
```

#### Using the walmart_get_product_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_get_product_detail_with_http_info(item_id)

```ruby
begin
  # Get product detail
  data, status_code, headers = api_instance.walmart_get_product_detail_with_http_info(item_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_product_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **String** | Walmart usItemId, e.g. &#39;5689919121&#39; |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## walmart_get_product_reviews

> Object walmart_get_product_reviews(item_id, opts)

Get product reviews

Paginated reviews with the full star histogram. 10 per page.

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

api_instance = ScrapeBadger::WalmartApi.new
item_id = 'item_id_example' # String | Walmart usItemId, e.g. '5689919121'
opts = {
  page: 56, # Integer | 
  sort: 'sort_example' # String | relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful
}

begin
  # Get product reviews
  result = api_instance.walmart_get_product_reviews(item_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_product_reviews: #{e}"
end
```

#### Using the walmart_get_product_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_get_product_reviews_with_http_info(item_id, opts)

```ruby
begin
  # Get product reviews
  data, status_code, headers = api_instance.walmart_get_product_reviews_with_http_info(item_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_product_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **String** | Walmart usItemId, e.g. &#39;5689919121&#39; |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **sort** | **String** | relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## walmart_get_seller_profile

> Object walmart_get_seller_profile(seller_id)

Get seller profile

Marketplace seller profile — contact details, address, rating, policies.  No `page`: adding one makes Walmart's own SSR throw. Use `/sellers/{id}/products` for the catalogue.

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

api_instance = ScrapeBadger::WalmartApi.new
seller_id = 'seller_id_example' # String | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).

begin
  # Get seller profile
  result = api_instance.walmart_get_seller_profile(seller_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_seller_profile: #{e}"
end
```

#### Using the walmart_get_seller_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_get_seller_profile_with_http_info(seller_id)

```ruby
begin
  # Get seller profile
  data, status_code, headers = api_instance.walmart_get_seller_profile_with_http_info(seller_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_seller_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **seller_id** | **String** | Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## walmart_get_store_nearby_stores

> Object walmart_get_store_nearby_stores(store_id)

Get store + nearby stores

Store detail with hours, per-department services, and nearby stores.

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

api_instance = ScrapeBadger::WalmartApi.new
store_id = 'store_id_example' # String | Walmart store number, e.g. '100'

begin
  # Get store + nearby stores
  result = api_instance.walmart_get_store_nearby_stores(store_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_store_nearby_stores: #{e}"
end
```

#### Using the walmart_get_store_nearby_stores_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_get_store_nearby_stores_with_http_info(store_id)

```ruby
begin
  # Get store + nearby stores
  data, status_code, headers = api_instance.walmart_get_store_nearby_stores_with_http_info(store_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_get_store_nearby_stores_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **store_id** | **String** | Walmart store number, e.g. &#39;100&#39; |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## walmart_list_supported_markets

> Object walmart_list_supported_markets

List supported markets

Supported Walmart markets.

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

api_instance = ScrapeBadger::WalmartApi.new

begin
  # List supported markets
  result = api_instance.walmart_list_supported_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_list_supported_markets: #{e}"
end
```

#### Using the walmart_list_supported_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_list_supported_markets_with_http_info

```ruby
begin
  # List supported markets
  data, status_code, headers = api_instance.walmart_list_supported_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_list_supported_markets_with_http_info: #{e}"
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


## walmart_search_products

> Object walmart_search_products(query, opts)

Search products

Search walmart.com. ~40-60 organic products per page; ad tiles are dropped.

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

api_instance = ScrapeBadger::WalmartApi.new
query = 'query_example' # String | Search keywords, e.g. 'laptop'
opts = {
  page: 56, # Integer | Results dry up after page 10
  sort: 'sort_example', # String | best_match | best_seller | price_low | price_high | rating_high | new
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  facet: 'facet_example' # String | Facet filter, e.g. 'brand:HP'
}

begin
  # Search products
  result = api_instance.walmart_search_products(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_search_products: #{e}"
end
```

#### Using the walmart_search_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_search_products_with_http_info(query, opts)

```ruby
begin
  # Search products
  data, status_code, headers = api_instance.walmart_search_products_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_search_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;laptop&#39; |  |
| **page** | **Integer** | Results dry up after page 10 | [optional][default to 1] |
| **sort** | **String** | best_match | best_seller | price_low | price_high | rating_high | new | [optional] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **facet** | **String** | Facet filter, e.g. &#39;brand:HP&#39; | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## walmart_search_suggestions

> Object walmart_search_suggestions(query)

Search suggestions

Walmart search-box suggestions.

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

api_instance = ScrapeBadger::WalmartApi.new
query = 'query_example' # String | Partial search term, e.g. 'lapt'

begin
  # Search suggestions
  result = api_instance.walmart_search_suggestions(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_search_suggestions: #{e}"
end
```

#### Using the walmart_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_search_suggestions_with_http_info(query)

```ruby
begin
  # Search suggestions
  data, status_code, headers = api_instance.walmart_search_suggestions_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial search term, e.g. &#39;lapt&#39; |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## walmart_walmart_scraper_health_check

> Object walmart_walmart_scraper_health_check

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::WalmartApi.new

begin
  # Walmart scraper health check
  result = api_instance.walmart_walmart_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_walmart_scraper_health_check: #{e}"
end
```

#### Using the walmart_walmart_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_walmart_scraper_health_check_with_http_info

```ruby
begin
  # Walmart scraper health check
  data, status_code, headers = api_instance.walmart_walmart_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_walmart_scraper_health_check_with_http_info: #{e}"
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


## walmart_walmart_scraper_health_check_head

> Object walmart_walmart_scraper_health_check_head

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::WalmartApi.new

begin
  # Walmart scraper health check
  result = api_instance.walmart_walmart_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_walmart_scraper_health_check_head: #{e}"
end
```

#### Using the walmart_walmart_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> walmart_walmart_scraper_health_check_head_with_http_info

```ruby
begin
  # Walmart scraper health check
  data, status_code, headers = api_instance.walmart_walmart_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WalmartApi->walmart_walmart_scraper_health_check_head_with_http_info: #{e}"
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

