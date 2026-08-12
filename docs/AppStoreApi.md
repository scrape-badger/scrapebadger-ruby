# ScrapeBadger::AppStoreApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**app_store_get_app_detail**](AppStoreApi.md#app_store_get_app_detail) | **GET** /v1/app-store/apps/{app_id} | Get app detail |
| [**app_store_get_app_reviews**](AppStoreApi.md#app_store_get_app_reviews) | **GET** /v1/app-store/apps/{app_id}/reviews | Get app reviews |
| [**app_store_get_developer_apps**](AppStoreApi.md#app_store_get_developer_apps) | **GET** /v1/app-store/developers/{artist_id} | Get developer apps |
| [**app_store_list_genres**](AppStoreApi.md#app_store_list_genres) | **GET** /v1/app-store/genres | List genres |
| [**app_store_list_markets**](AppStoreApi.md#app_store_list_markets) | **GET** /v1/app-store/markets | List markets |
| [**app_store_search_apps**](AppStoreApi.md#app_store_search_apps) | **GET** /v1/app-store/search | Search apps |
| [**app_store_top_charts**](AppStoreApi.md#app_store_top_charts) | **GET** /v1/app-store/charts | Top charts |


## app_store_get_app_detail

> Object app_store_get_app_detail(app_id, opts)

Get app detail

App detail: bundle id, version, pricing, ratings, genres, min OS, size, languages, screenshots, in-app purchases and version history.

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

api_instance = ScrapeBadger::AppStoreApi.new
app_id = 'app_id_example' # String | Numeric trackId (e.g. '310633997') or bundle id (e.g. 'net.whatsapp.WhatsApp').
opts = {
  country: 'country_example', # String | 
  lang: 'lang_example', # String | Result language, e.g. 'en_us'
  include_extras: true # Boolean | Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch.
}

begin
  # Get app detail
  result = api_instance.app_store_get_app_detail(app_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_get_app_detail: #{e}"
end
```

#### Using the app_store_get_app_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> app_store_get_app_detail_with_http_info(app_id, opts)

```ruby
begin
  # Get app detail
  data, status_code, headers = api_instance.app_store_get_app_detail_with_http_info(app_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_get_app_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **app_id** | **String** | Numeric trackId (e.g. &#39;310633997&#39;) or bundle id (e.g. &#39;net.whatsapp.WhatsApp&#39;). |  |
| **country** | **String** |  | [optional][default to &#39;us&#39;] |
| **lang** | **String** | Result language, e.g. &#39;en_us&#39; | [optional] |
| **include_extras** | **Boolean** | Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch. | [optional][default to true] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## app_store_get_app_reviews

> Object app_store_get_app_reviews(app_id, opts)

Get app reviews

Paginated customer reviews (50 per page, up to 10 pages).

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

api_instance = ScrapeBadger::AppStoreApi.new
app_id = 'app_id_example' # String | Numeric trackId, e.g. '310633997'
opts = {
  country: 'country_example', # String | 
  page: 56, # Integer | Apple caps reviews at 10 pages
  sort: 'sort_example' # String | mostRecent | mostHelpful
}

begin
  # Get app reviews
  result = api_instance.app_store_get_app_reviews(app_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_get_app_reviews: #{e}"
end
```

#### Using the app_store_get_app_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> app_store_get_app_reviews_with_http_info(app_id, opts)

```ruby
begin
  # Get app reviews
  data, status_code, headers = api_instance.app_store_get_app_reviews_with_http_info(app_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_get_app_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **app_id** | **String** | Numeric trackId, e.g. &#39;310633997&#39; |  |
| **country** | **String** |  | [optional][default to &#39;us&#39;] |
| **page** | **Integer** | Apple caps reviews at 10 pages | [optional][default to 1] |
| **sort** | **String** | mostRecent | mostHelpful | [optional][default to &#39;mostRecent&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## app_store_get_developer_apps

> Object app_store_get_developer_apps(artist_id, opts)

Get developer apps

Developer info and their published apps.

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

api_instance = ScrapeBadger::AppStoreApi.new
artist_id = 'artist_id_example' # String | Numeric artistId (developer id)
opts = {
  country: 'country_example' # String | 
}

begin
  # Get developer apps
  result = api_instance.app_store_get_developer_apps(artist_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_get_developer_apps: #{e}"
end
```

#### Using the app_store_get_developer_apps_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> app_store_get_developer_apps_with_http_info(artist_id, opts)

```ruby
begin
  # Get developer apps
  data, status_code, headers = api_instance.app_store_get_developer_apps_with_http_info(artist_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_get_developer_apps_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **artist_id** | **String** | Numeric artistId (developer id) |  |
| **country** | **String** |  | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## app_store_list_genres

> Object app_store_list_genres

List genres

The Apple App Store genre/category ids.

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

api_instance = ScrapeBadger::AppStoreApi.new

begin
  # List genres
  result = api_instance.app_store_list_genres
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_list_genres: #{e}"
end
```

#### Using the app_store_list_genres_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> app_store_list_genres_with_http_info

```ruby
begin
  # List genres
  data, status_code, headers = api_instance.app_store_list_genres_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_list_genres_with_http_info: #{e}"
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


## app_store_list_markets

> Object app_store_list_markets

List markets

Supported App Store country codes.

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

api_instance = ScrapeBadger::AppStoreApi.new

begin
  # List markets
  result = api_instance.app_store_list_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_list_markets: #{e}"
end
```

#### Using the app_store_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> app_store_list_markets_with_http_info

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.app_store_list_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_list_markets_with_http_info: #{e}"
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


## app_store_search_apps

> Object app_store_search_apps(query, opts)

Search apps

Search the Apple App Store.

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

api_instance = ScrapeBadger::AppStoreApi.new
query = 'query_example' # String | Search term, e.g. 'chat'
opts = {
  country: 'country_example', # String | App Store country code
  entity: 'entity_example', # String | software | iPadSoftware | macSoftware
  limit: 56, # Integer | 
  offset: 56, # Integer | 
  lang: 'lang_example' # String | Language, e.g. 'en_us'
}

begin
  # Search apps
  result = api_instance.app_store_search_apps(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_search_apps: #{e}"
end
```

#### Using the app_store_search_apps_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> app_store_search_apps_with_http_info(query, opts)

```ruby
begin
  # Search apps
  data, status_code, headers = api_instance.app_store_search_apps_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_search_apps_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search term, e.g. &#39;chat&#39; |  |
| **country** | **String** | App Store country code | [optional][default to &#39;us&#39;] |
| **entity** | **String** | software | iPadSoftware | macSoftware | [optional][default to &#39;software&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **offset** | **Integer** |  | [optional][default to 0] |
| **lang** | **String** | Language, e.g. &#39;en_us&#39; | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## app_store_top_charts

> Object app_store_top_charts(opts)

Top charts

Top charts, optionally scoped to a genre.

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

api_instance = ScrapeBadger::AppStoreApi.new
opts = {
  country: 'country_example', # String | 
  type: 'type_example', # String | top-free | top-paid | top-grossing
  genre: 56, # Integer | Apple genre id (optional), e.g. 6014
  limit: 56, # Integer | 
  entity: 'entity_example' # String | apps (iPhone) | ipad
}

begin
  # Top charts
  result = api_instance.app_store_top_charts(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_top_charts: #{e}"
end
```

#### Using the app_store_top_charts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> app_store_top_charts_with_http_info(opts)

```ruby
begin
  # Top charts
  data, status_code, headers = api_instance.app_store_top_charts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AppStoreApi->app_store_top_charts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country** | **String** |  | [optional][default to &#39;us&#39;] |
| **type** | **String** | top-free | top-paid | top-grossing | [optional][default to &#39;top-free&#39;] |
| **genre** | **Integer** | Apple genre id (optional), e.g. 6014 | [optional] |
| **limit** | **Integer** |  | [optional][default to 50] |
| **entity** | **String** | apps (iPhone) | ipad | [optional][default to &#39;apps&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

