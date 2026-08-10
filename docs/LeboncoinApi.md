# ScrapeBadger::LeboncoinApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**leboncoin_get_a_seller_s_ads**](LeboncoinApi.md#leboncoin_get_a_seller_s_ads) | **GET** /v1/leboncoin/sellers/{user_id}/listings | Get a seller&#39;s ads |
| [**leboncoin_get_ad_detail**](LeboncoinApi.md#leboncoin_get_ad_detail) | **GET** /v1/leboncoin/ads/{list_id} | Get ad detail |
| [**leboncoin_get_seller_profile**](LeboncoinApi.md#leboncoin_get_seller_profile) | **GET** /v1/leboncoin/sellers/{user_id} | Get seller profile |
| [**leboncoin_get_similar_ads**](LeboncoinApi.md#leboncoin_get_similar_ads) | **GET** /v1/leboncoin/ads/{list_id}/similar | Get similar ads |
| [**leboncoin_leboncoin_scraper_health_check**](LeboncoinApi.md#leboncoin_leboncoin_scraper_health_check) | **GET** /v1/leboncoin/health | Leboncoin scraper health check |
| [**leboncoin_leboncoin_scraper_health_check_head**](LeboncoinApi.md#leboncoin_leboncoin_scraper_health_check_head) | **HEAD** /v1/leboncoin/health | Leboncoin scraper health check |
| [**leboncoin_list_categories**](LeboncoinApi.md#leboncoin_list_categories) | **GET** /v1/leboncoin/categories | List categories |
| [**leboncoin_list_departments**](LeboncoinApi.md#leboncoin_list_departments) | **GET** /v1/leboncoin/departments | List departments |
| [**leboncoin_list_markets**](LeboncoinApi.md#leboncoin_list_markets) | **GET** /v1/leboncoin/markets | List markets |
| [**leboncoin_list_regions**](LeboncoinApi.md#leboncoin_list_regions) | **GET** /v1/leboncoin/regions | List regions |
| [**leboncoin_location_autocomplete**](LeboncoinApi.md#leboncoin_location_autocomplete) | **GET** /v1/leboncoin/locations/search | Location autocomplete |
| [**leboncoin_search_leboncoin_ads**](LeboncoinApi.md#leboncoin_search_leboncoin_ads) | **GET** /v1/leboncoin/search | Search Leboncoin ads |


## leboncoin_get_a_seller_s_ads

> Object leboncoin_get_a_seller_s_ads(user_id, opts)

Get a seller's ads

A seller's active ads.

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

api_instance = ScrapeBadger::LeboncoinApi.new
user_id = 'user_id_example' # String | 
opts = {
  page: 56, # Integer | 
  limit: 56 # Integer | 
}

begin
  # Get a seller's ads
  result = api_instance.leboncoin_get_a_seller_s_ads(user_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_get_a_seller_s_ads: #{e}"
end
```

#### Using the leboncoin_get_a_seller_s_ads_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_get_a_seller_s_ads_with_http_info(user_id, opts)

```ruby
begin
  # Get a seller's ads
  data, status_code, headers = api_instance.leboncoin_get_a_seller_s_ads_with_http_info(user_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_get_a_seller_s_ads_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **limit** | **Integer** |  | [optional][default to 35] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## leboncoin_get_ad_detail

> Object leboncoin_get_ad_detail(list_id)

Get ad detail

Full detail for a Leboncoin ad.

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

api_instance = ScrapeBadger::LeboncoinApi.new
list_id = 56 # Integer | 

begin
  # Get ad detail
  result = api_instance.leboncoin_get_ad_detail(list_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_get_ad_detail: #{e}"
end
```

#### Using the leboncoin_get_ad_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_get_ad_detail_with_http_info(list_id)

```ruby
begin
  # Get ad detail
  data, status_code, headers = api_instance.leboncoin_get_ad_detail_with_http_info(list_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_get_ad_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list_id** | **Integer** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## leboncoin_get_seller_profile

> Object leboncoin_get_seller_profile(user_id)

Get seller profile

Public seller/pro-store profile.

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

api_instance = ScrapeBadger::LeboncoinApi.new
user_id = 'user_id_example' # String | 

begin
  # Get seller profile
  result = api_instance.leboncoin_get_seller_profile(user_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_get_seller_profile: #{e}"
end
```

#### Using the leboncoin_get_seller_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_get_seller_profile_with_http_info(user_id)

```ruby
begin
  # Get seller profile
  data, status_code, headers = api_instance.leboncoin_get_seller_profile_with_http_info(user_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_get_seller_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## leboncoin_get_similar_ads

> Object leboncoin_get_similar_ads(list_id, opts)

Get similar ads

Ads Leboncoin surfaces as similar to the given ad.

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

api_instance = ScrapeBadger::LeboncoinApi.new
list_id = 56 # Integer | 
opts = {
  limit: 56 # Integer | 
}

begin
  # Get similar ads
  result = api_instance.leboncoin_get_similar_ads(list_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_get_similar_ads: #{e}"
end
```

#### Using the leboncoin_get_similar_ads_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_get_similar_ads_with_http_info(list_id, opts)

```ruby
begin
  # Get similar ads
  data, status_code, headers = api_instance.leboncoin_get_similar_ads_with_http_info(list_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_get_similar_ads_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list_id** | **Integer** |  |  |
| **limit** | **Integer** |  | [optional][default to 20] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## leboncoin_leboncoin_scraper_health_check

> Object leboncoin_leboncoin_scraper_health_check

Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::LeboncoinApi.new

begin
  # Leboncoin scraper health check
  result = api_instance.leboncoin_leboncoin_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_leboncoin_scraper_health_check: #{e}"
end
```

#### Using the leboncoin_leboncoin_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_leboncoin_scraper_health_check_with_http_info

```ruby
begin
  # Leboncoin scraper health check
  data, status_code, headers = api_instance.leboncoin_leboncoin_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_leboncoin_scraper_health_check_with_http_info: #{e}"
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


## leboncoin_leboncoin_scraper_health_check_head

> Object leboncoin_leboncoin_scraper_health_check_head

Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::LeboncoinApi.new

begin
  # Leboncoin scraper health check
  result = api_instance.leboncoin_leboncoin_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_leboncoin_scraper_health_check_head: #{e}"
end
```

#### Using the leboncoin_leboncoin_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_leboncoin_scraper_health_check_head_with_http_info

```ruby
begin
  # Leboncoin scraper health check
  data, status_code, headers = api_instance.leboncoin_leboncoin_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_leboncoin_scraper_health_check_head_with_http_info: #{e}"
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


## leboncoin_list_categories

> Object leboncoin_list_categories

List categories

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

api_instance = ScrapeBadger::LeboncoinApi.new

begin
  # List categories
  result = api_instance.leboncoin_list_categories
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_list_categories: #{e}"
end
```

#### Using the leboncoin_list_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_list_categories_with_http_info

```ruby
begin
  # List categories
  data, status_code, headers = api_instance.leboncoin_list_categories_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_list_categories_with_http_info: #{e}"
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


## leboncoin_list_departments

> Object leboncoin_list_departments(opts)

List departments

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

api_instance = ScrapeBadger::LeboncoinApi.new
opts = {
  region_id: 'region_id_example' # String | 
}

begin
  # List departments
  result = api_instance.leboncoin_list_departments(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_list_departments: #{e}"
end
```

#### Using the leboncoin_list_departments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_list_departments_with_http_info(opts)

```ruby
begin
  # List departments
  data, status_code, headers = api_instance.leboncoin_list_departments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_list_departments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **region_id** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## leboncoin_list_markets

> Object leboncoin_list_markets

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

api_instance = ScrapeBadger::LeboncoinApi.new

begin
  # List markets
  result = api_instance.leboncoin_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_list_markets: #{e}"
end
```

#### Using the leboncoin_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.leboncoin_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_list_markets_with_http_info: #{e}"
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


## leboncoin_list_regions

> Object leboncoin_list_regions

List regions

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

api_instance = ScrapeBadger::LeboncoinApi.new

begin
  # List regions
  result = api_instance.leboncoin_list_regions
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_list_regions: #{e}"
end
```

#### Using the leboncoin_list_regions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_list_regions_with_http_info

```ruby
begin
  # List regions
  data, status_code, headers = api_instance.leboncoin_list_regions_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_list_regions_with_http_info: #{e}"
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


## leboncoin_location_autocomplete

> Object leboncoin_location_autocomplete(q)

Location autocomplete

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

api_instance = ScrapeBadger::LeboncoinApi.new
q = 'q_example' # String | Place name

begin
  # Location autocomplete
  result = api_instance.leboncoin_location_autocomplete(q)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_location_autocomplete: #{e}"
end
```

#### Using the leboncoin_location_autocomplete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_location_autocomplete_with_http_info(q)

```ruby
begin
  # Location autocomplete
  data, status_code, headers = api_instance.leboncoin_location_autocomplete_with_http_info(q)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_location_autocomplete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Place name |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## leboncoin_search_leboncoin_ads

> Object leboncoin_search_leboncoin_ads(opts)

Search Leboncoin ads

Search Leboncoin classifieds (France; scope by region/department/city).

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

api_instance = ScrapeBadger::LeboncoinApi.new
opts = {
  text: 'text_example', # String | Free-text query
  category: 'category_example', # String | Category id (see /categories)
  region_id: 'region_id_example', # String | Region id (see /regions)
  department_id: 'department_id_example', # String | Department id, e.g. 75
  city: 'city_example', # String | 
  zipcode: 'zipcode_example', # String | 
  price_min: 56, # Integer | 
  price_max: 56, # Integer | 
  owner_type: 'owner_type_example', # String | all | pro | private
  ad_type: 'ad_type_example', # String | offer | demand
  sort: 'sort_example', # String | relevance|newest|oldest|price_low|price_high
  page: 56, # Integer | 
  limit: 56 # Integer | 
}

begin
  # Search Leboncoin ads
  result = api_instance.leboncoin_search_leboncoin_ads(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_search_leboncoin_ads: #{e}"
end
```

#### Using the leboncoin_search_leboncoin_ads_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> leboncoin_search_leboncoin_ads_with_http_info(opts)

```ruby
begin
  # Search Leboncoin ads
  data, status_code, headers = api_instance.leboncoin_search_leboncoin_ads_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LeboncoinApi->leboncoin_search_leboncoin_ads_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | Free-text query | [optional] |
| **category** | **String** | Category id (see /categories) | [optional] |
| **region_id** | **String** | Region id (see /regions) | [optional] |
| **department_id** | **String** | Department id, e.g. 75 | [optional] |
| **city** | **String** |  | [optional] |
| **zipcode** | **String** |  | [optional] |
| **price_min** | **Integer** |  | [optional] |
| **price_max** | **Integer** |  | [optional] |
| **owner_type** | **String** | all | pro | private | [optional][default to &#39;all&#39;] |
| **ad_type** | **String** | offer | demand | [optional][default to &#39;offer&#39;] |
| **sort** | **String** | relevance|newest|oldest|price_low|price_high | [optional][default to &#39;relevance&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **limit** | **Integer** |  | [optional][default to 35] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

