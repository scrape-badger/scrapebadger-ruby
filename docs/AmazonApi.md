# ScrapeBadger::AmazonApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**amazon_amazon_scraper_health_check**](AmazonApi.md#amazon_amazon_scraper_health_check) | **GET** /v1/amazon/health | Amazon scraper health check |
| [**amazon_amazon_scraper_health_check_head**](AmazonApi.md#amazon_amazon_scraper_health_check_head) | **HEAD** /v1/amazon/health | Amazon scraper health check |
| [**amazon_bestsellers_by_category**](AmazonApi.md#amazon_bestsellers_by_category) | **GET** /v1/amazon/bestsellers | Bestsellers by category |
| [**amazon_browse_node_category_listing**](AmazonApi.md#amazon_browse_node_category_listing) | **GET** /v1/amazon/category | Browse-node category listing |
| [**amazon_get_all_seller_offers_buybox**](AmazonApi.md#amazon_get_all_seller_offers_buybox) | **GET** /v1/amazon/products/{asin}/offers | Get all seller offers (buybox) |
| [**amazon_get_product_detail**](AmazonApi.md#amazon_get_product_detail) | **GET** /v1/amazon/products/{asin} | Get product detail |
| [**amazon_get_product_reviews**](AmazonApi.md#amazon_get_product_reviews) | **GET** /v1/amazon/products/{asin}/reviews | Get product reviews |
| [**amazon_get_seller_feedback**](AmazonApi.md#amazon_get_seller_feedback) | **GET** /v1/amazon/sellers/{seller_id}/feedback | Get seller feedback |
| [**amazon_get_seller_profile**](AmazonApi.md#amazon_get_seller_profile) | **GET** /v1/amazon/sellers/{seller_id} | Get seller profile |
| [**amazon_get_seller_storefront_products**](AmazonApi.md#amazon_get_seller_storefront_products) | **GET** /v1/amazon/sellers/{seller_id}/products | Get seller storefront products |
| [**amazon_keyword_suggestions**](AmazonApi.md#amazon_keyword_suggestions) | **GET** /v1/amazon/autocomplete | Keyword suggestions |
| [**amazon_list_category_aliases**](AmazonApi.md#amazon_list_category_aliases) | **GET** /v1/amazon/categories | List category aliases |
| [**amazon_list_marketplaces**](AmazonApi.md#amazon_list_marketplaces) | **GET** /v1/amazon/markets | List marketplaces |
| [**amazon_new_releases_by_category**](AmazonApi.md#amazon_new_releases_by_category) | **GET** /v1/amazon/new-releases | New releases by category |
| [**amazon_search_amazon_products**](AmazonApi.md#amazon_search_amazon_products) | **GET** /v1/amazon/search | Search Amazon products |
| [**amazon_today_s_deals**](AmazonApi.md#amazon_today_s_deals) | **GET** /v1/amazon/deals | Today&#39;s deals |


## amazon_amazon_scraper_health_check

> Object amazon_amazon_scraper_health_check

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::AmazonApi.new

begin
  # Amazon scraper health check
  result = api_instance.amazon_amazon_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_amazon_scraper_health_check: #{e}"
end
```

#### Using the amazon_amazon_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_amazon_scraper_health_check_with_http_info

```ruby
begin
  # Amazon scraper health check
  data, status_code, headers = api_instance.amazon_amazon_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_amazon_scraper_health_check_with_http_info: #{e}"
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


## amazon_amazon_scraper_health_check_head

> Object amazon_amazon_scraper_health_check_head

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::AmazonApi.new

begin
  # Amazon scraper health check
  result = api_instance.amazon_amazon_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_amazon_scraper_health_check_head: #{e}"
end
```

#### Using the amazon_amazon_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_amazon_scraper_health_check_head_with_http_info

```ruby
begin
  # Amazon scraper health check
  data, status_code, headers = api_instance.amazon_amazon_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_amazon_scraper_health_check_head_with_http_info: #{e}"
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


## amazon_bestsellers_by_category

> Object amazon_bestsellers_by_category(opts)

Bestsellers by category

Top-selling products for a category (browse node).

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

api_instance = ScrapeBadger::AmazonApi.new
opts = {
  domain: 'domain_example', # String | 
  category: 'category_example', # String | Bestsellers node id or slug
  page: 56 # Integer | 
}

begin
  # Bestsellers by category
  result = api_instance.amazon_bestsellers_by_category(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_bestsellers_by_category: #{e}"
end
```

#### Using the amazon_bestsellers_by_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_bestsellers_by_category_with_http_info(opts)

```ruby
begin
  # Bestsellers by category
  data, status_code, headers = api_instance.amazon_bestsellers_by_category_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_bestsellers_by_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **category** | **String** | Bestsellers node id or slug | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_browse_node_category_listing

> Object amazon_browse_node_category_listing(node, opts)

Browse-node category listing

List products within an Amazon browse-node category.

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

api_instance = ScrapeBadger::AmazonApi.new
node = 'node_example' # String | Amazon browse-node id
opts = {
  domain: 'domain_example', # String | 
  page: 56, # Integer | 
  sort_by: 'sort_by_example' # String | 
}

begin
  # Browse-node category listing
  result = api_instance.amazon_browse_node_category_listing(node, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_browse_node_category_listing: #{e}"
end
```

#### Using the amazon_browse_node_category_listing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_browse_node_category_listing_with_http_info(node, opts)

```ruby
begin
  # Browse-node category listing
  data, status_code, headers = api_instance.amazon_browse_node_category_listing_with_http_info(node, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_browse_node_category_listing_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **node** | **String** | Amazon browse-node id |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **sort_by** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_get_all_seller_offers_buybox

> Object amazon_get_all_seller_offers_buybox(asin, opts)

Get all seller offers (buybox)

All third-party offers for an ASIN, including the Buy Box winner.

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

api_instance = ScrapeBadger::AmazonApi.new
asin = 'asin_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  zip: 'zip_example' # String | 
}

begin
  # Get all seller offers (buybox)
  result = api_instance.amazon_get_all_seller_offers_buybox(asin, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_all_seller_offers_buybox: #{e}"
end
```

#### Using the amazon_get_all_seller_offers_buybox_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_get_all_seller_offers_buybox_with_http_info(asin, opts)

```ruby
begin
  # Get all seller offers (buybox)
  data, status_code, headers = api_instance.amazon_get_all_seller_offers_buybox_with_http_info(asin, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_all_seller_offers_buybox_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **asin** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **zip** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_get_product_detail

> Object amazon_get_product_detail(asin, opts)

Get product detail

Full product detail by ASIN (price, variants, badges, buybox, ranks…).

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

api_instance = ScrapeBadger::AmazonApi.new
asin = 'asin_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  zip: 'zip_example', # String | Delivery postal/zip for localized buybox
  language: 'language_example' # String | 
}

begin
  # Get product detail
  result = api_instance.amazon_get_product_detail(asin, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_product_detail: #{e}"
end
```

#### Using the amazon_get_product_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_get_product_detail_with_http_info(asin, opts)

```ruby
begin
  # Get product detail
  data, status_code, headers = api_instance.amazon_get_product_detail_with_http_info(asin, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_product_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **asin** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **zip** | **String** | Delivery postal/zip for localized buybox | [optional] |
| **language** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_get_product_reviews

> Object amazon_get_product_reviews(asin, opts)

Get product reviews

Customer reviews for an ASIN (featured + paginated, with filters).

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

api_instance = ScrapeBadger::AmazonApi.new
asin = 'asin_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  page: 56, # Integer | Review page (1-100, ~10 reviews/page)
  sort_by: 'sort_by_example', # String | helpful | recent
  star: 'star_example', # String | one_star..five_star | positive | critical
  verified_only: true, # Boolean | 
  media_only: true # Boolean | 
}

begin
  # Get product reviews
  result = api_instance.amazon_get_product_reviews(asin, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_product_reviews: #{e}"
end
```

#### Using the amazon_get_product_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_get_product_reviews_with_http_info(asin, opts)

```ruby
begin
  # Get product reviews
  data, status_code, headers = api_instance.amazon_get_product_reviews_with_http_info(asin, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_product_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **asin** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** | Review page (1-100, ~10 reviews/page) | [optional][default to 1] |
| **sort_by** | **String** | helpful | recent | [optional][default to &#39;helpful&#39;] |
| **star** | **String** | one_star..five_star | positive | critical | [optional] |
| **verified_only** | **Boolean** |  | [optional][default to false] |
| **media_only** | **Boolean** |  | [optional][default to false] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_get_seller_feedback

> Object amazon_get_seller_feedback(seller_id, opts)

Get seller feedback

Buyer feedback entries for a seller.

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

api_instance = ScrapeBadger::AmazonApi.new
seller_id = 'seller_id_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  page: 56 # Integer | 
}

begin
  # Get seller feedback
  result = api_instance.amazon_get_seller_feedback(seller_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_seller_feedback: #{e}"
end
```

#### Using the amazon_get_seller_feedback_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_get_seller_feedback_with_http_info(seller_id, opts)

```ruby
begin
  # Get seller feedback
  data, status_code, headers = api_instance.amazon_get_seller_feedback_with_http_info(seller_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_seller_feedback_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **seller_id** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_get_seller_profile

> Object amazon_get_seller_profile(seller_id, opts)

Get seller profile

Seller profile, ratings and feedback summary.

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

api_instance = ScrapeBadger::AmazonApi.new
seller_id = 'seller_id_example' # String | 
opts = {
  domain: 'domain_example' # String | 
}

begin
  # Get seller profile
  result = api_instance.amazon_get_seller_profile(seller_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_seller_profile: #{e}"
end
```

#### Using the amazon_get_seller_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_get_seller_profile_with_http_info(seller_id, opts)

```ruby
begin
  # Get seller profile
  data, status_code, headers = api_instance.amazon_get_seller_profile_with_http_info(seller_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_seller_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **seller_id** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_get_seller_storefront_products

> Object amazon_get_seller_storefront_products(seller_id, opts)

Get seller storefront products

Products listed in a seller's storefront.

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

api_instance = ScrapeBadger::AmazonApi.new
seller_id = 'seller_id_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  page: 56 # Integer | 
}

begin
  # Get seller storefront products
  result = api_instance.amazon_get_seller_storefront_products(seller_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_seller_storefront_products: #{e}"
end
```

#### Using the amazon_get_seller_storefront_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_get_seller_storefront_products_with_http_info(seller_id, opts)

```ruby
begin
  # Get seller storefront products
  data, status_code, headers = api_instance.amazon_get_seller_storefront_products_with_http_info(seller_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_get_seller_storefront_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **seller_id** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_keyword_suggestions

> Object amazon_keyword_suggestions(query, opts)

Keyword suggestions

Get Amazon search autocomplete suggestions for keyword research.

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

api_instance = ScrapeBadger::AmazonApi.new
query = 'query_example' # String | Partial search term
opts = {
  domain: 'domain_example' # String | 
}

begin
  # Keyword suggestions
  result = api_instance.amazon_keyword_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_keyword_suggestions: #{e}"
end
```

#### Using the amazon_keyword_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_keyword_suggestions_with_http_info(query, opts)

```ruby
begin
  # Keyword suggestions
  data, status_code, headers = api_instance.amazon_keyword_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_keyword_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial search term |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_list_category_aliases

> Object amazon_list_category_aliases(opts)

List category aliases

List common Amazon department/category aliases and bestseller nodes.

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

api_instance = ScrapeBadger::AmazonApi.new
opts = {
  domain: 'domain_example' # String | 
}

begin
  # List category aliases
  result = api_instance.amazon_list_category_aliases(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_list_category_aliases: #{e}"
end
```

#### Using the amazon_list_category_aliases_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_list_category_aliases_with_http_info(opts)

```ruby
begin
  # List category aliases
  data, status_code, headers = api_instance.amazon_list_category_aliases_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_list_category_aliases_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_list_marketplaces

> Object amazon_list_marketplaces

List marketplaces

List all supported Amazon marketplaces.

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

api_instance = ScrapeBadger::AmazonApi.new

begin
  # List marketplaces
  result = api_instance.amazon_list_marketplaces
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_list_marketplaces: #{e}"
end
```

#### Using the amazon_list_marketplaces_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_list_marketplaces_with_http_info

```ruby
begin
  # List marketplaces
  data, status_code, headers = api_instance.amazon_list_marketplaces_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_list_marketplaces_with_http_info: #{e}"
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


## amazon_new_releases_by_category

> Object amazon_new_releases_by_category(opts)

New releases by category

Newly released products for a category (browse node).

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

api_instance = ScrapeBadger::AmazonApi.new
opts = {
  domain: 'domain_example', # String | 
  category: 'category_example', # String | 
  page: 56 # Integer | 
}

begin
  # New releases by category
  result = api_instance.amazon_new_releases_by_category(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_new_releases_by_category: #{e}"
end
```

#### Using the amazon_new_releases_by_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_new_releases_by_category_with_http_info(opts)

```ruby
begin
  # New releases by category
  data, status_code, headers = api_instance.amazon_new_releases_by_category_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_new_releases_by_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **category** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_search_amazon_products

> Object amazon_search_amazon_products(query, opts)

Search Amazon products

Search the Amazon catalog with filters and sorting.

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

api_instance = ScrapeBadger::AmazonApi.new
query = 'query_example' # String | Search keywords
opts = {
  domain: 'domain_example', # String | Amazon marketplace TLD or code (com, co.uk, de…)
  page: 56, # Integer | 
  sort_by: 'sort_by_example', # String | relevance | price_low_to_high | price_high_to_low | avg_review | newest
  category: 'category_example', # String | Department/category alias (i= param)
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  zip: 'zip_example', # String | Delivery postal/zip code for localized pricing
  language: 'language_example' # String | Locale for results, e.g. en_US, fr_FR
}

begin
  # Search Amazon products
  result = api_instance.amazon_search_amazon_products(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_search_amazon_products: #{e}"
end
```

#### Using the amazon_search_amazon_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_search_amazon_products_with_http_info(query, opts)

```ruby
begin
  # Search Amazon products
  data, status_code, headers = api_instance.amazon_search_amazon_products_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_search_amazon_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords |  |
| **domain** | **String** | Amazon marketplace TLD or code (com, co.uk, de…) | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **sort_by** | **String** | relevance | price_low_to_high | price_high_to_low | avg_review | newest | [optional] |
| **category** | **String** | Department/category alias (i&#x3D; param) | [optional] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **zip** | **String** | Delivery postal/zip code for localized pricing | [optional] |
| **language** | **String** | Locale for results, e.g. en_US, fr_FR | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## amazon_today_s_deals

> Object amazon_today_s_deals(opts)

Today's deals

Current Amazon deals (lightning deals, best deals).

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

api_instance = ScrapeBadger::AmazonApi.new
opts = {
  domain: 'domain_example', # String | 
  category: 'category_example', # String | 
  page: 56 # Integer | 
}

begin
  # Today's deals
  result = api_instance.amazon_today_s_deals(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_today_s_deals: #{e}"
end
```

#### Using the amazon_today_s_deals_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> amazon_today_s_deals_with_http_info(opts)

```ruby
begin
  # Today's deals
  data, status_code, headers = api_instance.amazon_today_s_deals_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AmazonApi->amazon_today_s_deals_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **category** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

