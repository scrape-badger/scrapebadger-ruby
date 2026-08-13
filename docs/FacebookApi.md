# ScrapeBadger::FacebookApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**facebook_browse_a_marketplace_category**](FacebookApi.md#facebook_browse_a_marketplace_category) | **GET** /v1/facebook/marketplace/category/{category} | Browse a Marketplace category |
| [**facebook_get_a_marketplace_item**](FacebookApi.md#facebook_get_a_marketplace_item) | **GET** /v1/facebook/marketplace/item/{item_id} | Get a Marketplace item |
| [**facebook_get_advertiser_page_info**](FacebookApi.md#facebook_get_advertiser_page_info) | **GET** /v1/facebook/ads/pages/{page_id} | Get advertiser page info |
| [**facebook_get_an_ad**](FacebookApi.md#facebook_get_an_ad) | **GET** /v1/facebook/ads/{ad_archive_id} | Get an ad |
| [**facebook_get_group_detail**](FacebookApi.md#facebook_get_group_detail) | **GET** /v1/facebook/groups/{group_id} | Get group detail |
| [**facebook_get_group_posts**](FacebookApi.md#facebook_get_group_posts) | **GET** /v1/facebook/groups/{group_id}/posts | Get group posts |
| [**facebook_get_page_detail**](FacebookApi.md#facebook_get_page_detail) | **GET** /v1/facebook/pages/{identifier} | Get page detail |
| [**facebook_get_page_posts**](FacebookApi.md#facebook_get_page_posts) | **GET** /v1/facebook/pages/{identifier}/posts | Get page posts |
| [**facebook_get_post_comments**](FacebookApi.md#facebook_get_post_comments) | **GET** /v1/facebook/posts/{post_id}/comments | Get post comments |
| [**facebook_get_post_detail**](FacebookApi.md#facebook_get_post_detail) | **GET** /v1/facebook/posts/{post_id} | Get post detail |
| [**facebook_get_profile_detail**](FacebookApi.md#facebook_get_profile_detail) | **GET** /v1/facebook/profiles/{identifier} | Get profile detail |
| [**facebook_get_profile_posts**](FacebookApi.md#facebook_get_profile_posts) | **GET** /v1/facebook/profiles/{identifier}/posts | Get profile posts |
| [**facebook_list_categories**](FacebookApi.md#facebook_list_categories) | **GET** /v1/facebook/marketplace/categories | List categories |
| [**facebook_list_locations**](FacebookApi.md#facebook_list_locations) | **GET** /v1/facebook/marketplace/locations | List locations |
| [**facebook_search_advertiser_pages**](FacebookApi.md#facebook_search_advertiser_pages) | **GET** /v1/facebook/ads/pages/search | Search advertiser pages |
| [**facebook_search_events**](FacebookApi.md#facebook_search_events) | **GET** /v1/facebook/search/events | Search events |
| [**facebook_search_everything**](FacebookApi.md#facebook_search_everything) | **GET** /v1/facebook/search | Search everything |
| [**facebook_search_groups**](FacebookApi.md#facebook_search_groups) | **GET** /v1/facebook/search/groups | Search groups |
| [**facebook_search_marketplace**](FacebookApi.md#facebook_search_marketplace) | **GET** /v1/facebook/marketplace/search | Search Marketplace |
| [**facebook_search_pages**](FacebookApi.md#facebook_search_pages) | **GET** /v1/facebook/search/pages | Search Pages |
| [**facebook_search_people**](FacebookApi.md#facebook_search_people) | **GET** /v1/facebook/search/people | Search people |
| [**facebook_search_places**](FacebookApi.md#facebook_search_places) | **GET** /v1/facebook/search/places | Search places |
| [**facebook_search_posts**](FacebookApi.md#facebook_search_posts) | **GET** /v1/facebook/search/posts | Search posts |
| [**facebook_search_the_ad_library**](FacebookApi.md#facebook_search_the_ad_library) | **GET** /v1/facebook/ads/search | Search the Ad Library |


## facebook_browse_a_marketplace_category

> Object facebook_browse_a_marketplace_category(category, opts)

Browse a Marketplace category

Browse Marketplace listings in a category (vehicles, electronics, ...).

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

api_instance = ScrapeBadger::FacebookApi.new
category = 'category_example' # String | 
opts = {
  location: 'location_example', # String | 
  min_price: 56, # Integer | 
  max_price: 56, # Integer | 
  sort_by: 'sort_by_example', # String | 
  after: 'after_example' # String | 
}

begin
  # Browse a Marketplace category
  result = api_instance.facebook_browse_a_marketplace_category(category, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_browse_a_marketplace_category: #{e}"
end
```

#### Using the facebook_browse_a_marketplace_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_browse_a_marketplace_category_with_http_info(category, opts)

```ruby
begin
  # Browse a Marketplace category
  data, status_code, headers = api_instance.facebook_browse_a_marketplace_category_with_http_info(category, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_browse_a_marketplace_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category** | **String** |  |  |
| **location** | **String** |  | [optional][default to &#39;nyc&#39;] |
| **min_price** | **Integer** |  | [optional] |
| **max_price** | **Integer** |  | [optional] |
| **sort_by** | **String** |  | [optional] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_a_marketplace_item

> Object facebook_get_a_marketplace_item(item_id)

Get a Marketplace item

Get full detail for a single Marketplace listing.

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

api_instance = ScrapeBadger::FacebookApi.new
item_id = 'item_id_example' # String | 

begin
  # Get a Marketplace item
  result = api_instance.facebook_get_a_marketplace_item(item_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_a_marketplace_item: #{e}"
end
```

#### Using the facebook_get_a_marketplace_item_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_a_marketplace_item_with_http_info(item_id)

```ruby
begin
  # Get a Marketplace item
  data, status_code, headers = api_instance.facebook_get_a_marketplace_item_with_http_info(item_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_a_marketplace_item_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_advertiser_page_info

> Object facebook_get_advertiser_page_info(page_id, opts)

Get advertiser page info

Get advertiser page info: category, followers, page transparency (creation date, name history, managing organization, admin-account locations), related pages, and ad spend (for political/issue advertisers).

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

api_instance = ScrapeBadger::FacebookApi.new
page_id = 'page_id_example' # String | 
opts = {
  country: 'country_example' # String | 
}

begin
  # Get advertiser page info
  result = api_instance.facebook_get_advertiser_page_info(page_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_advertiser_page_info: #{e}"
end
```

#### Using the facebook_get_advertiser_page_info_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_advertiser_page_info_with_http_info(page_id, opts)

```ruby
begin
  # Get advertiser page info
  data, status_code, headers = api_instance.facebook_get_advertiser_page_info_with_http_info(page_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_advertiser_page_info_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_id** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_an_ad

> Object facebook_get_an_ad(ad_archive_id, opts)

Get an ad

Get a single Ad Library ad by its archive id. For EU/UK-targeted ads the response also includes transparency insights (payer/beneficiary, total EU reach, and age/gender/country reach breakdowns).

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

api_instance = ScrapeBadger::FacebookApi.new
ad_archive_id = 'ad_archive_id_example' # String | 
opts = {
  country: 'country_example' # String | ISO country code (an EU code returns EU transparency)
}

begin
  # Get an ad
  result = api_instance.facebook_get_an_ad(ad_archive_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_an_ad: #{e}"
end
```

#### Using the facebook_get_an_ad_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_an_ad_with_http_info(ad_archive_id, opts)

```ruby
begin
  # Get an ad
  data, status_code, headers = api_instance.facebook_get_an_ad_with_http_info(ad_archive_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_an_ad_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ad_archive_id** | **String** |  |  |
| **country** | **String** | ISO country code (an EU code returns EU transparency) | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_group_detail

> Object facebook_get_group_detail(group_id)

Get group detail

Get a Facebook group's details.

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

api_instance = ScrapeBadger::FacebookApi.new
group_id = 'group_id_example' # String | 

begin
  # Get group detail
  result = api_instance.facebook_get_group_detail(group_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_group_detail: #{e}"
end
```

#### Using the facebook_get_group_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_group_detail_with_http_info(group_id)

```ruby
begin
  # Get group detail
  data, status_code, headers = api_instance.facebook_get_group_detail_with_http_info(group_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_group_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **group_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_group_posts

> Object facebook_get_group_posts(group_id, opts)

Get group posts

Get a Facebook group's post feed.

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

api_instance = ScrapeBadger::FacebookApi.new
group_id = 'group_id_example' # String | 
opts = {
  after: 'after_example' # String | 
}

begin
  # Get group posts
  result = api_instance.facebook_get_group_posts(group_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_group_posts: #{e}"
end
```

#### Using the facebook_get_group_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_group_posts_with_http_info(group_id, opts)

```ruby
begin
  # Get group posts
  data, status_code, headers = api_instance.facebook_get_group_posts_with_http_info(group_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_group_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **group_id** | **String** |  |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_page_detail

> Object facebook_get_page_detail(identifier)

Get page detail

Get a Facebook Page's profile (name, category, followers, about).

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

api_instance = ScrapeBadger::FacebookApi.new
identifier = 'identifier_example' # String | 

begin
  # Get page detail
  result = api_instance.facebook_get_page_detail(identifier)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_page_detail: #{e}"
end
```

#### Using the facebook_get_page_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_page_detail_with_http_info(identifier)

```ruby
begin
  # Get page detail
  data, status_code, headers = api_instance.facebook_get_page_detail_with_http_info(identifier)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_page_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_page_posts

> Object facebook_get_page_posts(identifier, opts)

Get page posts

Get a Facebook Page's timeline posts.

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

api_instance = ScrapeBadger::FacebookApi.new
identifier = 'identifier_example' # String | 
opts = {
  after: 'after_example' # String | 
}

begin
  # Get page posts
  result = api_instance.facebook_get_page_posts(identifier, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_page_posts: #{e}"
end
```

#### Using the facebook_get_page_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_page_posts_with_http_info(identifier, opts)

```ruby
begin
  # Get page posts
  data, status_code, headers = api_instance.facebook_get_page_posts_with_http_info(identifier, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_page_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** |  |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_post_comments

> Object facebook_get_post_comments(post_id, opts)

Get post comments

Get a Facebook post's comment thread (paginated).

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

api_instance = ScrapeBadger::FacebookApi.new
post_id = 'post_id_example' # String | 
opts = {
  after: 'after_example', # String | 
  sort: 'sort_example' # String | 
}

begin
  # Get post comments
  result = api_instance.facebook_get_post_comments(post_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_post_comments: #{e}"
end
```

#### Using the facebook_get_post_comments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_post_comments_with_http_info(post_id, opts)

```ruby
begin
  # Get post comments
  data, status_code, headers = api_instance.facebook_get_post_comments_with_http_info(post_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_post_comments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |
| **after** | **String** |  | [optional] |
| **sort** | **String** |  | [optional][default to &#39;relevance&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_post_detail

> Object facebook_get_post_detail(post_id)

Get post detail

Get a Facebook post's detail plus its top comments.

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

api_instance = ScrapeBadger::FacebookApi.new
post_id = 'post_id_example' # String | 

begin
  # Get post detail
  result = api_instance.facebook_get_post_detail(post_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_post_detail: #{e}"
end
```

#### Using the facebook_get_post_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_post_detail_with_http_info(post_id)

```ruby
begin
  # Get post detail
  data, status_code, headers = api_instance.facebook_get_post_detail_with_http_info(post_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_post_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_profile_detail

> Object facebook_get_profile_detail(identifier)

Get profile detail

Get a Facebook profile's details.

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

api_instance = ScrapeBadger::FacebookApi.new
identifier = 'identifier_example' # String | 

begin
  # Get profile detail
  result = api_instance.facebook_get_profile_detail(identifier)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_profile_detail: #{e}"
end
```

#### Using the facebook_get_profile_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_profile_detail_with_http_info(identifier)

```ruby
begin
  # Get profile detail
  data, status_code, headers = api_instance.facebook_get_profile_detail_with_http_info(identifier)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_profile_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_get_profile_posts

> Object facebook_get_profile_posts(identifier, opts)

Get profile posts

Get a Facebook profile's timeline posts.

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

api_instance = ScrapeBadger::FacebookApi.new
identifier = 'identifier_example' # String | 
opts = {
  after: 'after_example' # String | 
}

begin
  # Get profile posts
  result = api_instance.facebook_get_profile_posts(identifier, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_profile_posts: #{e}"
end
```

#### Using the facebook_get_profile_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_get_profile_posts_with_http_info(identifier, opts)

```ruby
begin
  # Get profile posts
  data, status_code, headers = api_instance.facebook_get_profile_posts_with_http_info(identifier, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_get_profile_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** |  |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_list_categories

> Object facebook_list_categories

List categories

List Marketplace category slugs (free).

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

api_instance = ScrapeBadger::FacebookApi.new

begin
  # List categories
  result = api_instance.facebook_list_categories
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_list_categories: #{e}"
end
```

#### Using the facebook_list_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_list_categories_with_http_info

```ruby
begin
  # List categories
  data, status_code, headers = api_instance.facebook_list_categories_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_list_categories_with_http_info: #{e}"
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


## facebook_list_locations

> Object facebook_list_locations

List locations

List common Marketplace location slugs (free).

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

api_instance = ScrapeBadger::FacebookApi.new

begin
  # List locations
  result = api_instance.facebook_list_locations
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_list_locations: #{e}"
end
```

#### Using the facebook_list_locations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_list_locations_with_http_info

```ruby
begin
  # List locations
  data, status_code, headers = api_instance.facebook_list_locations_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_list_locations_with_http_info: #{e}"
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


## facebook_search_advertiser_pages

> Object facebook_search_advertiser_pages(query, opts)

Search advertiser pages

Search advertiser Pages in the Ad Library — returns page ids, categories, likes/followers, verification and Instagram handles.

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

api_instance = ScrapeBadger::FacebookApi.new
query = 'query_example' # String | Advertiser name or keyword
opts = {
  country: 'country_example' # String | 
}

begin
  # Search advertiser pages
  result = api_instance.facebook_search_advertiser_pages(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_advertiser_pages: #{e}"
end
```

#### Using the facebook_search_advertiser_pages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_advertiser_pages_with_http_info(query, opts)

```ruby
begin
  # Search advertiser pages
  data, status_code, headers = api_instance.facebook_search_advertiser_pages_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_advertiser_pages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Advertiser name or keyword |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_search_events

> Object facebook_search_events(q, opts)

Search events

Search Facebook events.

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

api_instance = ScrapeBadger::FacebookApi.new
q = 'q_example' # String | 
opts = {
  after: 'after_example' # String | 
}

begin
  # Search events
  result = api_instance.facebook_search_events(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_events: #{e}"
end
```

#### Using the facebook_search_events_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_events_with_http_info(q, opts)

```ruby
begin
  # Search events
  data, status_code, headers = api_instance.facebook_search_events_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_events_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** |  |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_search_everything

> Object facebook_search_everything(q, opts)

Search everything

Global Facebook search (top results across pages, people, groups, posts).

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

api_instance = ScrapeBadger::FacebookApi.new
q = 'q_example' # String | Search query
opts = {
  after: 'after_example' # String | 
}

begin
  # Search everything
  result = api_instance.facebook_search_everything(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_everything: #{e}"
end
```

#### Using the facebook_search_everything_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_everything_with_http_info(q, opts)

```ruby
begin
  # Search everything
  data, status_code, headers = api_instance.facebook_search_everything_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_everything_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_search_groups

> Object facebook_search_groups(q, opts)

Search groups

Search Facebook groups.

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

api_instance = ScrapeBadger::FacebookApi.new
q = 'q_example' # String | 
opts = {
  after: 'after_example' # String | 
}

begin
  # Search groups
  result = api_instance.facebook_search_groups(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_groups: #{e}"
end
```

#### Using the facebook_search_groups_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_groups_with_http_info(q, opts)

```ruby
begin
  # Search groups
  data, status_code, headers = api_instance.facebook_search_groups_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_groups_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** |  |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_search_marketplace

> Object facebook_search_marketplace(query, opts)

Search Marketplace

Search Facebook Marketplace listings by keyword and location.

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

api_instance = ScrapeBadger::FacebookApi.new
query = 'query_example' # String | Search keywords
opts = {
  location: 'location_example', # String | Marketplace location slug
  min_price: 56, # Integer | 
  max_price: 56, # Integer | 
  days_since_listed: 56, # Integer | 
  sort_by: 'sort_by_example', # String | 
  item_condition: 'item_condition_example', # String | 
  delivery_method: 'delivery_method_example', # String | 
  after: 'after_example' # String | 
}

begin
  # Search Marketplace
  result = api_instance.facebook_search_marketplace(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_marketplace: #{e}"
end
```

#### Using the facebook_search_marketplace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_marketplace_with_http_info(query, opts)

```ruby
begin
  # Search Marketplace
  data, status_code, headers = api_instance.facebook_search_marketplace_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_marketplace_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords |  |
| **location** | **String** | Marketplace location slug | [optional][default to &#39;nyc&#39;] |
| **min_price** | **Integer** |  | [optional] |
| **max_price** | **Integer** |  | [optional] |
| **days_since_listed** | **Integer** |  | [optional] |
| **sort_by** | **String** |  | [optional] |
| **item_condition** | **String** |  | [optional] |
| **delivery_method** | **String** |  | [optional] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_search_pages

> Object facebook_search_pages(q, opts)

Search Pages

Search Facebook Pages.

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

api_instance = ScrapeBadger::FacebookApi.new
q = 'q_example' # String | 
opts = {
  after: 'after_example' # String | 
}

begin
  # Search Pages
  result = api_instance.facebook_search_pages(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_pages: #{e}"
end
```

#### Using the facebook_search_pages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_pages_with_http_info(q, opts)

```ruby
begin
  # Search Pages
  data, status_code, headers = api_instance.facebook_search_pages_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_pages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** |  |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_search_people

> Object facebook_search_people(q, opts)

Search people

Search Facebook profiles.

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

api_instance = ScrapeBadger::FacebookApi.new
q = 'q_example' # String | 
opts = {
  after: 'after_example' # String | 
}

begin
  # Search people
  result = api_instance.facebook_search_people(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_people: #{e}"
end
```

#### Using the facebook_search_people_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_people_with_http_info(q, opts)

```ruby
begin
  # Search people
  data, status_code, headers = api_instance.facebook_search_people_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_people_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** |  |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_search_places

> Object facebook_search_places(q, opts)

Search places

Search Facebook places.

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

api_instance = ScrapeBadger::FacebookApi.new
q = 'q_example' # String | 
opts = {
  after: 'after_example' # String | 
}

begin
  # Search places
  result = api_instance.facebook_search_places(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_places: #{e}"
end
```

#### Using the facebook_search_places_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_places_with_http_info(q, opts)

```ruby
begin
  # Search places
  data, status_code, headers = api_instance.facebook_search_places_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_places_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** |  |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_search_posts

> Object facebook_search_posts(q, opts)

Search posts

Search public Facebook posts.

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

api_instance = ScrapeBadger::FacebookApi.new
q = 'q_example' # String | 
opts = {
  after: 'after_example' # String | 
}

begin
  # Search posts
  result = api_instance.facebook_search_posts(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_posts: #{e}"
end
```

#### Using the facebook_search_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_posts_with_http_info(q, opts)

```ruby
begin
  # Search posts
  data, status_code, headers = api_instance.facebook_search_posts_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** |  |  |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## facebook_search_the_ad_library

> Object facebook_search_the_ad_library(query, opts)

Search the Ad Library

Search the Facebook Ad Library.

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

api_instance = ScrapeBadger::FacebookApi.new
query = 'query_example' # String | Advertiser or keyword
opts = {
  country: 'country_example', # String | 
  ad_type: 'ad_type_example', # String | 
  active_status: 'active_status_example', # String | 
  after: 'after_example' # String | 
}

begin
  # Search the Ad Library
  result = api_instance.facebook_search_the_ad_library(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_the_ad_library: #{e}"
end
```

#### Using the facebook_search_the_ad_library_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> facebook_search_the_ad_library_with_http_info(query, opts)

```ruby
begin
  # Search the Ad Library
  data, status_code, headers = api_instance.facebook_search_the_ad_library_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FacebookApi->facebook_search_the_ad_library_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Advertiser or keyword |  |
| **country** | **String** |  | [optional][default to &#39;US&#39;] |
| **ad_type** | **String** |  | [optional][default to &#39;all&#39;] |
| **active_status** | **String** |  | [optional][default to &#39;active&#39;] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

