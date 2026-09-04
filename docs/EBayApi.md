# ScrapeBadger::EBayApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**ebay_browse_a_category**](EBayApi.md#ebay_browse_a_category) | **GET** /v1/ebay/categories/{category_id}/items | Browse a category |
| [**ebay_completed_sold_listings**](EBayApi.md#ebay_completed_sold_listings) | **GET** /v1/ebay/completed | Completed / sold listings |
| [**ebay_ebay_scraper_health_check**](EBayApi.md#ebay_ebay_scraper_health_check) | **GET** /v1/ebay/health | eBay scraper health check |
| [**ebay_ebay_scraper_health_check_head**](EBayApi.md#ebay_ebay_scraper_health_check_head) | **HEAD** /v1/ebay/health | eBay scraper health check |
| [**ebay_get_item_detail**](EBayApi.md#ebay_get_item_detail) | **GET** /v1/ebay/items/{item_id} | Get item detail |
| [**ebay_get_item_reviews**](EBayApi.md#ebay_get_item_reviews) | **GET** /v1/ebay/items/{item_id}/reviews | Get item reviews |
| [**ebay_get_seller_feedback**](EBayApi.md#ebay_get_seller_feedback) | **GET** /v1/ebay/sellers/{username}/feedback | Get seller feedback |
| [**ebay_get_seller_listings**](EBayApi.md#ebay_get_seller_listings) | **GET** /v1/ebay/sellers/{username}/items | Get seller listings |
| [**ebay_get_seller_profile**](EBayApi.md#ebay_get_seller_profile) | **GET** /v1/ebay/sellers/{username} | Get seller profile |
| [**ebay_keyword_suggestions**](EBayApi.md#ebay_keyword_suggestions) | **GET** /v1/ebay/autocomplete | Keyword suggestions |
| [**ebay_list_categories**](EBayApi.md#ebay_list_categories) | **GET** /v1/ebay/categories | List categories |
| [**ebay_list_markets**](EBayApi.md#ebay_list_markets) | **GET** /v1/ebay/markets | List markets |
| [**ebay_search_listings**](EBayApi.md#ebay_search_listings) | **GET** /v1/ebay/search | Search listings |


## ebay_browse_a_category

> Object ebay_browse_a_category(category_id, opts)

Browse a category

List active listings within an eBay category.

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

api_instance = ScrapeBadger::EBayApi.new
category_id = 'category_id_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  page: 56, # Integer | 
  per_page: 56, # Integer | 
  sort_by: 'sort_by_example', # String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
  min_price: 8.14, # Float | 
  max_price: 8.14 # Float | 
}

begin
  # Browse a category
  result = api_instance.ebay_browse_a_category(category_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_browse_a_category: #{e}"
end
```

#### Using the ebay_browse_a_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_browse_a_category_with_http_info(category_id, opts)

```ruby
begin
  # Browse a category
  data, status_code, headers = api_instance.ebay_browse_a_category_with_http_info(category_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_browse_a_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** |  | [optional] |
| **sort_by** | **String** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional][default to &#39;best_match&#39;] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ebay_completed_sold_listings

> Object ebay_completed_sold_listings(query, opts)

Completed / sold listings

Search completed/sold listings — eBay's sold-price history.

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

api_instance = ScrapeBadger::EBayApi.new
query = 'query_example' # String | Search keywords
opts = {
  domain: 'domain_example', # String | Marketplace domain (com, co.uk, de …)
  category_id: 'category_id_example', # String | Restrict to a category id
  page: 56, # Integer | 
  per_page: 56, # Integer | 60, 120 or 240
  sort_by: 'sort_by_example', # String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
  condition: 'condition_example', # String | new|open_box|refurbished|used|for_parts|graded|ungraded
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  location: 'location_example', # String | domestic|worldwide
  language: 'language_example' # String | english|japanese|chinese|korean
}

begin
  # Completed / sold listings
  result = api_instance.ebay_completed_sold_listings(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_completed_sold_listings: #{e}"
end
```

#### Using the ebay_completed_sold_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_completed_sold_listings_with_http_info(query, opts)

```ruby
begin
  # Completed / sold listings
  data, status_code, headers = api_instance.ebay_completed_sold_listings_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_completed_sold_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords |  |
| **domain** | **String** | Marketplace domain (com, co.uk, de …) | [optional][default to &#39;com&#39;] |
| **category_id** | **String** | Restrict to a category id | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** | 60, 120 or 240 | [optional] |
| **sort_by** | **String** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional][default to &#39;best_match&#39;] |
| **condition** | **String** | new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **location** | **String** | domestic|worldwide | [optional] |
| **language** | **String** | english|japanese|chinese|korean | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ebay_ebay_scraper_health_check

> Object ebay_ebay_scraper_health_check

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::EBayApi.new

begin
  # eBay scraper health check
  result = api_instance.ebay_ebay_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_ebay_scraper_health_check: #{e}"
end
```

#### Using the ebay_ebay_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_ebay_scraper_health_check_with_http_info

```ruby
begin
  # eBay scraper health check
  data, status_code, headers = api_instance.ebay_ebay_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_ebay_scraper_health_check_with_http_info: #{e}"
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


## ebay_ebay_scraper_health_check_head

> Object ebay_ebay_scraper_health_check_head

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::EBayApi.new

begin
  # eBay scraper health check
  result = api_instance.ebay_ebay_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_ebay_scraper_health_check_head: #{e}"
end
```

#### Using the ebay_ebay_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_ebay_scraper_health_check_head_with_http_info

```ruby
begin
  # eBay scraper health check
  data, status_code, headers = api_instance.ebay_ebay_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_ebay_scraper_health_check_head_with_http_info: #{e}"
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


## ebay_get_item_detail

> Object ebay_get_item_detail(item_id, opts)

Get item detail

Get a single eBay listing's full detail.

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

api_instance = ScrapeBadger::EBayApi.new
item_id = 'item_id_example' # String | 
opts = {
  domain: 'domain_example' # String | 
}

begin
  # Get item detail
  result = api_instance.ebay_get_item_detail(item_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_item_detail: #{e}"
end
```

#### Using the ebay_get_item_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_item_detail_with_http_info(item_id, opts)

```ruby
begin
  # Get item detail
  data, status_code, headers = api_instance.ebay_get_item_detail_with_http_info(item_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_item_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ebay_get_item_reviews

> Object ebay_get_item_reviews(item_id, opts)

Get item reviews

Get catalog product reviews shown on an eBay listing.

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

api_instance = ScrapeBadger::EBayApi.new
item_id = 'item_id_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  page: 56 # Integer | 
}

begin
  # Get item reviews
  result = api_instance.ebay_get_item_reviews(item_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_item_reviews: #{e}"
end
```

#### Using the ebay_get_item_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_item_reviews_with_http_info(item_id, opts)

```ruby
begin
  # Get item reviews
  data, status_code, headers = api_instance.ebay_get_item_reviews_with_http_info(item_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_item_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ebay_get_seller_feedback

> Object ebay_get_seller_feedback(username, opts)

Get seller feedback

Get a seller's recent feedback comments.

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

api_instance = ScrapeBadger::EBayApi.new
username = 'username_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  page: 56 # Integer | 
}

begin
  # Get seller feedback
  result = api_instance.ebay_get_seller_feedback(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_feedback: #{e}"
end
```

#### Using the ebay_get_seller_feedback_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_seller_feedback_with_http_info(username, opts)

```ruby
begin
  # Get seller feedback
  data, status_code, headers = api_instance.ebay_get_seller_feedback_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_feedback_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ebay_get_seller_listings

> Object ebay_get_seller_listings(username, opts)

Get seller listings

List the active listings of a single eBay seller.

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

api_instance = ScrapeBadger::EBayApi.new
username = 'username_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  query: 'query_example', # String | 
  page: 56, # Integer | 
  per_page: 56 # Integer | 
}

begin
  # Get seller listings
  result = api_instance.ebay_get_seller_listings(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_listings: #{e}"
end
```

#### Using the ebay_get_seller_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_seller_listings_with_http_info(username, opts)

```ruby
begin
  # Get seller listings
  data, status_code, headers = api_instance.ebay_get_seller_listings_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **query** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ebay_get_seller_profile

> Object ebay_get_seller_profile(username, opts)

Get seller profile

Get an eBay seller's public profile.

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

api_instance = ScrapeBadger::EBayApi.new
username = 'username_example' # String | 
opts = {
  domain: 'domain_example' # String | 
}

begin
  # Get seller profile
  result = api_instance.ebay_get_seller_profile(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_profile: #{e}"
end
```

#### Using the ebay_get_seller_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_seller_profile_with_http_info(username, opts)

```ruby
begin
  # Get seller profile
  data, status_code, headers = api_instance.ebay_get_seller_profile_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ebay_keyword_suggestions

> Object ebay_keyword_suggestions(query, opts)

Keyword suggestions

Return eBay keyword autocomplete suggestions.

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

api_instance = ScrapeBadger::EBayApi.new
query = 'query_example' # String | Partial query prefix
opts = {
  domain: 'domain_example' # String | 
}

begin
  # Keyword suggestions
  result = api_instance.ebay_keyword_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_keyword_suggestions: #{e}"
end
```

#### Using the ebay_keyword_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_keyword_suggestions_with_http_info(query, opts)

```ruby
begin
  # Keyword suggestions
  data, status_code, headers = api_instance.ebay_keyword_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_keyword_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial query prefix |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ebay_list_categories

> Object ebay_list_categories

List categories

List eBay's top-level category ids.

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

api_instance = ScrapeBadger::EBayApi.new

begin
  # List categories
  result = api_instance.ebay_list_categories
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_list_categories: #{e}"
end
```

#### Using the ebay_list_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_list_categories_with_http_info

```ruby
begin
  # List categories
  data, status_code, headers = api_instance.ebay_list_categories_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_list_categories_with_http_info: #{e}"
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


## ebay_list_markets

> Object ebay_list_markets

List markets

List all supported eBay marketplaces.

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

api_instance = ScrapeBadger::EBayApi.new

begin
  # List markets
  result = api_instance.ebay_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_list_markets: #{e}"
end
```

#### Using the ebay_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.ebay_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_list_markets_with_http_info: #{e}"
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


## ebay_search_listings

> Object ebay_search_listings(query, opts)

Search listings

Search an eBay marketplace for active listings.

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

api_instance = ScrapeBadger::EBayApi.new
query = 'query_example' # String | Search keywords
opts = {
  domain: 'domain_example', # String | Marketplace domain (com, co.uk, de …)
  category_id: 'category_id_example', # String | Restrict to a category id
  page: 56, # Integer | 
  per_page: 56, # Integer | 60, 120 or 240
  sort_by: 'sort_by_example', # String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
  condition: 'condition_example', # String | new|open_box|refurbished|used|for_parts|graded|ungraded
  buying_format: 'buying_format_example', # String | auction|buy_it_now|best_offer
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  free_shipping: true, # Boolean | 
  location: 'location_example', # String | domestic|worldwide
  language: 'language_example' # String | english|japanese|chinese|korean
}

begin
  # Search listings
  result = api_instance.ebay_search_listings(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_search_listings: #{e}"
end
```

#### Using the ebay_search_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_search_listings_with_http_info(query, opts)

```ruby
begin
  # Search listings
  data, status_code, headers = api_instance.ebay_search_listings_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_search_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords |  |
| **domain** | **String** | Marketplace domain (com, co.uk, de …) | [optional][default to &#39;com&#39;] |
| **category_id** | **String** | Restrict to a category id | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** | 60, 120 or 240 | [optional] |
| **sort_by** | **String** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional][default to &#39;best_match&#39;] |
| **condition** | **String** | new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] |
| **buying_format** | **String** | auction|buy_it_now|best_offer | [optional] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **free_shipping** | **Boolean** |  | [optional][default to false] |
| **location** | **String** | domestic|worldwide | [optional] |
| **language** | **String** | english|japanese|chinese|korean | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

