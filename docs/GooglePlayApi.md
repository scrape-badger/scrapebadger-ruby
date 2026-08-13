# ScrapeBadger::GooglePlayApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**google_play_browse_a_category**](GooglePlayApi.md#google_play_browse_a_category) | **GET** /v1/google-play/categories/{category_id} | Browse a category |
| [**google_play_get_app_detail**](GooglePlayApi.md#google_play_get_app_detail) | **GET** /v1/google-play/apps/{app_id} | Get app detail |
| [**google_play_get_app_permissions**](GooglePlayApi.md#google_play_get_app_permissions) | **GET** /v1/google-play/apps/{app_id}/permissions | Get app permissions |
| [**google_play_get_app_reviews**](GooglePlayApi.md#google_play_get_app_reviews) | **GET** /v1/google-play/apps/{app_id}/reviews | Get app reviews |
| [**google_play_get_developer_apps**](GooglePlayApi.md#google_play_get_developer_apps) | **GET** /v1/google-play/developers/{developer} | Get developer apps |
| [**google_play_get_similar_apps**](GooglePlayApi.md#google_play_get_similar_apps) | **GET** /v1/google-play/apps/{app_id}/similar | Get similar apps |
| [**google_play_list_categories**](GooglePlayApi.md#google_play_list_categories) | **GET** /v1/google-play/categories | List categories |
| [**google_play_list_markets**](GooglePlayApi.md#google_play_list_markets) | **GET** /v1/google-play/markets | List markets |
| [**google_play_search_apps**](GooglePlayApi.md#google_play_search_apps) | **GET** /v1/google-play/search | Search apps |
| [**google_play_top_charts**](GooglePlayApi.md#google_play_top_charts) | **GET** /v1/google-play/collections/{collection} | Top charts |


## google_play_browse_a_category

> Object google_play_browse_a_category(category_id, opts)

Browse a category

The top apps within a Play category.

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

api_instance = ScrapeBadger::GooglePlayApi.new
category_id = 'category_id_example' # String | Play category id, e.g. 'GAME_PUZZLE' or 'SOCIAL'
opts = {
  country: 'country_example', # String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
  lang: 'lang_example', # String | Play content language (hl), e.g. 'en' or 'pt-BR'
  num: 56 # Integer | Max apps; follows each rail's 'see more' continuation above the ~40-120 the page renders directly
}

begin
  # Browse a category
  result = api_instance.google_play_browse_a_category(category_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_browse_a_category: #{e}"
end
```

#### Using the google_play_browse_a_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_browse_a_category_with_http_info(category_id, opts)

```ruby
begin
  # Browse a category
  data, status_code, headers = api_instance.google_play_browse_a_category_with_http_info(category_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_browse_a_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** | Play category id, e.g. &#39;GAME_PUZZLE&#39; or &#39;SOCIAL&#39; |  |
| **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional][default to &#39;US&#39;] |
| **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional][default to &#39;en&#39;] |
| **num** | **Integer** | Max apps; follows each rail&#39;s &#39;see more&#39; continuation above the ~40-120 the page renders directly | [optional][default to 100] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_play_get_app_detail

> Object google_play_get_app_detail(app_id, opts)

Get app detail

Full app detail: ratings histogram, installs, pricing, IAP, developer, screenshots, version metadata and what's-new.

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

api_instance = ScrapeBadger::GooglePlayApi.new
app_id = 'app_id_example' # String | Android package id, e.g. 'com.whatsapp'.
opts = {
  country: 'country_example', # String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
  lang: 'lang_example' # String | Play content language (hl), e.g. 'en' or 'pt-BR'
}

begin
  # Get app detail
  result = api_instance.google_play_get_app_detail(app_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_app_detail: #{e}"
end
```

#### Using the google_play_get_app_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_get_app_detail_with_http_info(app_id, opts)

```ruby
begin
  # Get app detail
  data, status_code, headers = api_instance.google_play_get_app_detail_with_http_info(app_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_app_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **app_id** | **String** | Android package id, e.g. &#39;com.whatsapp&#39;. |  |
| **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional][default to &#39;US&#39;] |
| **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_play_get_app_permissions

> Object google_play_get_app_permissions(app_id, opts)

Get app permissions

The app's requested Android permissions, grouped.

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

api_instance = ScrapeBadger::GooglePlayApi.new
app_id = 'app_id_example' # String | Android package id, e.g. 'com.whatsapp'.
opts = {
  lang: 'lang_example' # String | Play content language (hl), e.g. 'en' or 'pt-BR'
}

begin
  # Get app permissions
  result = api_instance.google_play_get_app_permissions(app_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_app_permissions: #{e}"
end
```

#### Using the google_play_get_app_permissions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_get_app_permissions_with_http_info(app_id, opts)

```ruby
begin
  # Get app permissions
  data, status_code, headers = api_instance.google_play_get_app_permissions_with_http_info(app_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_app_permissions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **app_id** | **String** | Android package id, e.g. &#39;com.whatsapp&#39;. |  |
| **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_play_get_app_reviews

> Object google_play_get_app_reviews(app_id, opts)

Get app reviews

Paginated app reviews via the Play batchexecute RPC.

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

api_instance = ScrapeBadger::GooglePlayApi.new
app_id = 'app_id_example' # String | Android package id, e.g. 'com.whatsapp'.
opts = {
  country: 'country_example', # String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
  lang: 'lang_example', # String | Play content language (hl), e.g. 'en' or 'pt-BR'
  sort: 'sort_example', # String | newest | rating | helpfulness
  count: 56, # Integer | 
  page_token: 'page_token_example' # String | Pagination token
}

begin
  # Get app reviews
  result = api_instance.google_play_get_app_reviews(app_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_app_reviews: #{e}"
end
```

#### Using the google_play_get_app_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_get_app_reviews_with_http_info(app_id, opts)

```ruby
begin
  # Get app reviews
  data, status_code, headers = api_instance.google_play_get_app_reviews_with_http_info(app_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_app_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **app_id** | **String** | Android package id, e.g. &#39;com.whatsapp&#39;. |  |
| **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional][default to &#39;US&#39;] |
| **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional][default to &#39;en&#39;] |
| **sort** | **String** | newest | rating | helpfulness | [optional][default to &#39;newest&#39;] |
| **count** | **Integer** |  | [optional][default to 40] |
| **page_token** | **String** | Pagination token | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_play_get_developer_apps

> Object google_play_get_developer_apps(developer, opts)

Get developer apps

A developer's published apps.

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

api_instance = ScrapeBadger::GooglePlayApi.new
developer = 'developer_example' # String | Developer name or numeric id
opts = {
  country: 'country_example', # String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
  lang: 'lang_example', # String | Play content language (hl), e.g. 'en' or 'pt-BR'
  num: 56 # Integer | Max apps; follows rail continuations above the page's directly-rendered slice
}

begin
  # Get developer apps
  result = api_instance.google_play_get_developer_apps(developer, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_developer_apps: #{e}"
end
```

#### Using the google_play_get_developer_apps_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_get_developer_apps_with_http_info(developer, opts)

```ruby
begin
  # Get developer apps
  data, status_code, headers = api_instance.google_play_get_developer_apps_with_http_info(developer, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_developer_apps_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **developer** | **String** | Developer name or numeric id |  |
| **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional][default to &#39;US&#39;] |
| **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional][default to &#39;en&#39;] |
| **num** | **Integer** | Max apps; follows rail continuations above the page&#39;s directly-rendered slice | [optional][default to 100] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_play_get_similar_apps

> Object google_play_get_similar_apps(app_id, opts)

Get similar apps

Apps Google Play lists as similar to this one.

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

api_instance = ScrapeBadger::GooglePlayApi.new
app_id = 'app_id_example' # String | Android package id, e.g. 'com.whatsapp'.
opts = {
  country: 'country_example', # String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
  lang: 'lang_example' # String | Play content language (hl), e.g. 'en' or 'pt-BR'
}

begin
  # Get similar apps
  result = api_instance.google_play_get_similar_apps(app_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_similar_apps: #{e}"
end
```

#### Using the google_play_get_similar_apps_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_get_similar_apps_with_http_info(app_id, opts)

```ruby
begin
  # Get similar apps
  data, status_code, headers = api_instance.google_play_get_similar_apps_with_http_info(app_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_get_similar_apps_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **app_id** | **String** | Android package id, e.g. &#39;com.whatsapp&#39;. |  |
| **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional][default to &#39;US&#39;] |
| **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_play_list_categories

> Object google_play_list_categories

List categories

The Google Play app/game category ids.

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

api_instance = ScrapeBadger::GooglePlayApi.new

begin
  # List categories
  result = api_instance.google_play_list_categories
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_list_categories: #{e}"
end
```

#### Using the google_play_list_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_list_categories_with_http_info

```ruby
begin
  # List categories
  data, status_code, headers = api_instance.google_play_list_categories_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_list_categories_with_http_info: #{e}"
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


## google_play_list_markets

> Object google_play_list_markets

List markets

Supported Google Play store countries and languages.

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

api_instance = ScrapeBadger::GooglePlayApi.new

begin
  # List markets
  result = api_instance.google_play_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_list_markets: #{e}"
end
```

#### Using the google_play_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.google_play_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_list_markets_with_http_info: #{e}"
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


## google_play_search_apps

> Object google_play_search_apps(query, opts)

Search apps

Search Google Play for apps and games (the ~30 server-rendered results; Play exposes no page parameter).

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

api_instance = ScrapeBadger::GooglePlayApi.new
query = 'query_example' # String | Search keywords, e.g. 'puzzle'
opts = {
  country: 'country_example', # String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
  lang: 'lang_example', # String | Play content language (hl), e.g. 'en' or 'pt-BR'
  price: 'price_example' # String | free | paid | all
}

begin
  # Search apps
  result = api_instance.google_play_search_apps(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_search_apps: #{e}"
end
```

#### Using the google_play_search_apps_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_search_apps_with_http_info(query, opts)

```ruby
begin
  # Search apps
  data, status_code, headers = api_instance.google_play_search_apps_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_search_apps_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;puzzle&#39; |  |
| **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional][default to &#39;US&#39;] |
| **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional][default to &#39;en&#39;] |
| **price** | **String** | free | paid | all | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_play_top_charts

> Object google_play_top_charts(collection, opts)

Top charts

Top charts for a collection, optionally scoped to a category.

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

api_instance = ScrapeBadger::GooglePlayApi.new
collection = 'collection_example' # String | topselling_free | topselling_paid | topgrossing
opts = {
  category: 'category_example', # String | Play category, e.g. 'GAME'
  country: 'country_example', # String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
  lang: 'lang_example' # String | Play content language (hl), e.g. 'en' or 'pt-BR'
}

begin
  # Top charts
  result = api_instance.google_play_top_charts(collection, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_top_charts: #{e}"
end
```

#### Using the google_play_top_charts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_play_top_charts_with_http_info(collection, opts)

```ruby
begin
  # Top charts
  data, status_code, headers = api_instance.google_play_top_charts_with_http_info(collection, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GooglePlayApi->google_play_top_charts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **collection** | **String** | topselling_free | topselling_paid | topgrossing |  |
| **category** | **String** | Play category, e.g. &#39;GAME&#39; | [optional][default to &#39;APPLICATION&#39;] |
| **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional][default to &#39;US&#39;] |
| **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

