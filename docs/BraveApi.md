# ScrapeBadger::BraveApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**brave_autocomplete**](BraveApi.md#brave_autocomplete) | **GET** /v1/brave/autocomplete | Autocomplete |
| [**brave_image_search**](BraveApi.md#brave_image_search) | **GET** /v1/brave/images | Image search |
| [**brave_list_supported_locales**](BraveApi.md#brave_list_supported_locales) | **GET** /v1/brave/locales | List supported locales |
| [**brave_news_search**](BraveApi.md#brave_news_search) | **GET** /v1/brave/news | News search |
| [**brave_video_search**](BraveApi.md#brave_video_search) | **GET** /v1/brave/videos | Video search |
| [**brave_web_search**](BraveApi.md#brave_web_search) | **GET** /v1/brave/search | Web search |


## brave_autocomplete

> <BraveAutocompleteResponse> brave_autocomplete(query, opts)

Autocomplete

Native search-box suggestions with entity descriptions and images. Two credits.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | 
opts = {
  country: 'us' # String | 
}

begin
  # Autocomplete
  result = api_instance.brave_autocomplete(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_autocomplete: #{e}"
end
```

#### Using the brave_autocomplete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveAutocompleteResponse>, Integer, Hash)> brave_autocomplete_with_http_info(query, opts)

```ruby
begin
  # Autocomplete
  data, status_code, headers = api_instance.brave_autocomplete_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveAutocompleteResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_autocomplete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;us&#39;] |

### Return type

[**BraveAutocompleteResponse**](BraveAutocompleteResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_image_search

> <BraveResponse> brave_image_search(query, opts)

Image search

Native image batch with original URLs, source pages, thumbnails and dimensions.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | Native Brave search query
opts = {
  country: 'us', # String | Native result region; see /locales
  ui_language: 'en-us', # String | UI labels/date language; does not restrict result language
  safe_search: 'off', # String | 
  count: 56 # Integer | Slice the initial native image batch
}

begin
  # Image search
  result = api_instance.brave_image_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_image_search: #{e}"
end
```

#### Using the brave_image_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveResponse>, Integer, Hash)> brave_image_search_with_http_info(query, opts)

```ruby
begin
  # Image search
  data, status_code, headers = api_instance.brave_image_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_image_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Native Brave search query |  |
| **country** | **String** | Native result region; see /locales | [optional][default to &#39;us&#39;] |
| **ui_language** | **String** | UI labels/date language; does not restrict result language | [optional][default to &#39;en-us&#39;] |
| **safe_search** | **String** |  | [optional][default to &#39;moderate&#39;] |
| **count** | **Integer** | Slice the initial native image batch | [optional][default to 50] |

### Return type

[**BraveResponse**](BraveResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_list_supported_locales

> <BraveLocalesResponse> brave_list_supported_locales

List supported locales

Native country and UI-language choices. Free; result language is a separate preference.

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

api_instance = ScrapeBadger::BraveApi.new

begin
  # List supported locales
  result = api_instance.brave_list_supported_locales
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_list_supported_locales: #{e}"
end
```

#### Using the brave_list_supported_locales_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveLocalesResponse>, Integer, Hash)> brave_list_supported_locales_with_http_info

```ruby
begin
  # List supported locales
  data, status_code, headers = api_instance.brave_list_supported_locales_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveLocalesResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_list_supported_locales_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BraveLocalesResponse**](BraveLocalesResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_news_search

> <BraveResponse> brave_news_search(query, opts)

News search

Native news batch; relative source dates stay display strings.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | Native Brave search query
opts = {
  country: 'us', # String | Native result region; see /locales
  ui_language: 'en-us', # String | UI labels/date language; does not restrict result language
  safe_search: 'off', # String | 
  count: 56 # Integer | Slice the initial native news batch
}

begin
  # News search
  result = api_instance.brave_news_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_news_search: #{e}"
end
```

#### Using the brave_news_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveResponse>, Integer, Hash)> brave_news_search_with_http_info(query, opts)

```ruby
begin
  # News search
  data, status_code, headers = api_instance.brave_news_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_news_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Native Brave search query |  |
| **country** | **String** | Native result region; see /locales | [optional][default to &#39;us&#39;] |
| **ui_language** | **String** | UI labels/date language; does not restrict result language | [optional][default to &#39;en-us&#39;] |
| **safe_search** | **String** |  | [optional][default to &#39;moderate&#39;] |
| **count** | **Integer** | Slice the initial native news batch | [optional][default to 35] |

### Return type

[**BraveResponse**](BraveResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_video_search

> <BravePagedResponse> brave_video_search(query, opts)

Video search

Native video results with duration, creator, publisher and verified page ordinals.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | Native Brave search query
opts = {
  country: 'us', # String | Native result region; see /locales
  ui_language: 'en-us', # String | UI labels/date language; does not restrict result language
  safe_search: 'off', # String | 
  page: 56, # Integer | 1-based native page ordinal
  count: 56 # Integer | 
}

begin
  # Video search
  result = api_instance.brave_video_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_video_search: #{e}"
end
```

#### Using the brave_video_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BravePagedResponse>, Integer, Hash)> brave_video_search_with_http_info(query, opts)

```ruby
begin
  # Video search
  data, status_code, headers = api_instance.brave_video_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BravePagedResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_video_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Native Brave search query |  |
| **country** | **String** | Native result region; see /locales | [optional][default to &#39;us&#39;] |
| **ui_language** | **String** | UI labels/date language; does not restrict result language | [optional][default to &#39;en-us&#39;] |
| **safe_search** | **String** |  | [optional][default to &#39;moderate&#39;] |
| **page** | **Integer** | 1-based native page ordinal | [optional][default to 1] |
| **count** | **Integer** |  | [optional][default to 50] |

### Return type

[**BravePagedResponse**](BravePagedResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_web_search

> <BraveSearchResponse> brave_web_search(query, opts)

Web search

Native Brave organic results, rich source blocks and page metadata. Seven credits.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | Native Brave search query
opts = {
  country: 'us', # String | Native result region; see /locales
  ui_language: 'en-us', # String | UI labels/date language; does not restrict result language
  safe_search: 'off', # String | 
  page: 56, # Integer | 1-based native page ordinal
  count: 56, # Integer | Slice one native page; does not change native page boundaries
  freshness: 'any', # String | 
  spellcheck: true # Boolean | Allow native spelling correction
}

begin
  # Web search
  result = api_instance.brave_web_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_web_search: #{e}"
end
```

#### Using the brave_web_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveSearchResponse>, Integer, Hash)> brave_web_search_with_http_info(query, opts)

```ruby
begin
  # Web search
  data, status_code, headers = api_instance.brave_web_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveSearchResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_web_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Native Brave search query |  |
| **country** | **String** | Native result region; see /locales | [optional][default to &#39;us&#39;] |
| **ui_language** | **String** | UI labels/date language; does not restrict result language | [optional][default to &#39;en-us&#39;] |
| **safe_search** | **String** |  | [optional][default to &#39;moderate&#39;] |
| **page** | **Integer** | 1-based native page ordinal | [optional][default to 1] |
| **count** | **Integer** | Slice one native page; does not change native page boundaries | [optional][default to 20] |
| **freshness** | **String** |  | [optional][default to &#39;any&#39;] |
| **spellcheck** | **Boolean** | Allow native spelling correction | [optional][default to false] |

### Return type

[**BraveSearchResponse**](BraveSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

