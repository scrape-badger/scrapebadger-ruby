# ScrapeBadger::DuckDuckGoApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**duckduckgo_duckduckgo_scraper_health_check**](DuckDuckGoApi.md#duckduckgo_duckduckgo_scraper_health_check) | **GET** /v1/duckduckgo/health | DuckDuckGo scraper health check |
| [**duckduckgo_duckduckgo_scraper_health_check_head**](DuckDuckGoApi.md#duckduckgo_duckduckgo_scraper_health_check_head) | **HEAD** /v1/duckduckgo/health | DuckDuckGo scraper health check |
| [**duckduckgo_image_search**](DuckDuckGoApi.md#duckduckgo_image_search) | **GET** /v1/duckduckgo/images | Image search |
| [**duckduckgo_instant_answer**](DuckDuckGoApi.md#duckduckgo_instant_answer) | **GET** /v1/duckduckgo/instant | Instant Answer |
| [**duckduckgo_list_supported_regions**](DuckDuckGoApi.md#duckduckgo_list_supported_regions) | **GET** /v1/duckduckgo/regions | List supported regions |
| [**duckduckgo_news_search**](DuckDuckGoApi.md#duckduckgo_news_search) | **GET** /v1/duckduckgo/news | News search |
| [**duckduckgo_search_suggestions**](DuckDuckGoApi.md#duckduckgo_search_suggestions) | **GET** /v1/duckduckgo/autocomplete | Search suggestions |
| [**duckduckgo_video_search**](DuckDuckGoApi.md#duckduckgo_video_search) | **GET** /v1/duckduckgo/videos | Video search |
| [**duckduckgo_web_search**](DuckDuckGoApi.md#duckduckgo_web_search) | **GET** /v1/duckduckgo/search | Web search |


## duckduckgo_duckduckgo_scraper_health_check

> Object duckduckgo_duckduckgo_scraper_health_check

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::DuckDuckGoApi.new

begin
  # DuckDuckGo scraper health check
  result = api_instance.duckduckgo_duckduckgo_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_duckduckgo_scraper_health_check: #{e}"
end
```

#### Using the duckduckgo_duckduckgo_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> duckduckgo_duckduckgo_scraper_health_check_with_http_info

```ruby
begin
  # DuckDuckGo scraper health check
  data, status_code, headers = api_instance.duckduckgo_duckduckgo_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_duckduckgo_scraper_health_check_with_http_info: #{e}"
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


## duckduckgo_duckduckgo_scraper_health_check_head

> Object duckduckgo_duckduckgo_scraper_health_check_head

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::DuckDuckGoApi.new

begin
  # DuckDuckGo scraper health check
  result = api_instance.duckduckgo_duckduckgo_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_duckduckgo_scraper_health_check_head: #{e}"
end
```

#### Using the duckduckgo_duckduckgo_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> duckduckgo_duckduckgo_scraper_health_check_head_with_http_info

```ruby
begin
  # DuckDuckGo scraper health check
  data, status_code, headers = api_instance.duckduckgo_duckduckgo_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_duckduckgo_scraper_health_check_head_with_http_info: #{e}"
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


## duckduckgo_image_search

> Object duckduckgo_image_search(query, opts)

Image search

DuckDuckGo image search with size/color/type/layout/license filters.

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

api_instance = ScrapeBadger::DuckDuckGoApi.new
query = 'query_example' # String | Search query
opts = {
  region: 'region_example', # String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
  safesearch: 'safesearch_example', # String | on | moderate | off
  page: 56, # Integer | 100 results per page
  size: 'size_example', # String | Small | Medium | Large | Wallpaper
  color: 'color_example', # String | color | Monochrome | Red | Blue | …
  image_type: 'image_type_example', # String | photo | clipart | gif | transparent | line
  layout: 'layout_example', # String | Square | Tall | Wide
  license: 'license_example' # String | Any | Public | Share | ShareCommercially | Modify
}

begin
  # Image search
  result = api_instance.duckduckgo_image_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_image_search: #{e}"
end
```

#### Using the duckduckgo_image_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> duckduckgo_image_search_with_http_info(query, opts)

```ruby
begin
  # Image search
  data, status_code, headers = api_instance.duckduckgo_image_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_image_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search query |  |
| **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional][default to &#39;wt-wt&#39;] |
| **safesearch** | **String** | on | moderate | off | [optional][default to &#39;moderate&#39;] |
| **page** | **Integer** | 100 results per page | [optional][default to 1] |
| **size** | **String** | Small | Medium | Large | Wallpaper | [optional][default to &#39;&#39;] |
| **color** | **String** | color | Monochrome | Red | Blue | … | [optional][default to &#39;&#39;] |
| **image_type** | **String** | photo | clipart | gif | transparent | line | [optional][default to &#39;&#39;] |
| **layout** | **String** | Square | Tall | Wide | [optional][default to &#39;&#39;] |
| **license** | **String** | Any | Public | Share | ShareCommercially | Modify | [optional][default to &#39;&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## duckduckgo_instant_answer

> Object duckduckgo_instant_answer(query)

Instant Answer

DuckDuckGo Instant Answer — abstract, definition, direct answer, related topics.

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

api_instance = ScrapeBadger::DuckDuckGoApi.new
query = 'query_example' # String | Query for the Instant Answer API

begin
  # Instant Answer
  result = api_instance.duckduckgo_instant_answer(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_instant_answer: #{e}"
end
```

#### Using the duckduckgo_instant_answer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> duckduckgo_instant_answer_with_http_info(query)

```ruby
begin
  # Instant Answer
  data, status_code, headers = api_instance.duckduckgo_instant_answer_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_instant_answer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Query for the Instant Answer API |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## duckduckgo_list_supported_regions

> Object duckduckgo_list_supported_regions

List supported regions

The full DuckDuckGo region (kl) code list.

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

api_instance = ScrapeBadger::DuckDuckGoApi.new

begin
  # List supported regions
  result = api_instance.duckduckgo_list_supported_regions
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_list_supported_regions: #{e}"
end
```

#### Using the duckduckgo_list_supported_regions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> duckduckgo_list_supported_regions_with_http_info

```ruby
begin
  # List supported regions
  data, status_code, headers = api_instance.duckduckgo_list_supported_regions_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_list_supported_regions_with_http_info: #{e}"
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


## duckduckgo_news_search

> Object duckduckgo_news_search(query, opts)

News search

DuckDuckGo news search — headline, source, excerpt, unix + ISO date, image.

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

api_instance = ScrapeBadger::DuckDuckGoApi.new
query = 'query_example' # String | Search query
opts = {
  region: 'region_example', # String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
  safesearch: 'safesearch_example', # String | on | moderate | off
  timelimit: 'timelimit_example', # String | day | week | month | year
  page: 56 # Integer | 30 results per page
}

begin
  # News search
  result = api_instance.duckduckgo_news_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_news_search: #{e}"
end
```

#### Using the duckduckgo_news_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> duckduckgo_news_search_with_http_info(query, opts)

```ruby
begin
  # News search
  data, status_code, headers = api_instance.duckduckgo_news_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_news_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search query |  |
| **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional][default to &#39;wt-wt&#39;] |
| **safesearch** | **String** | on | moderate | off | [optional][default to &#39;moderate&#39;] |
| **timelimit** | **String** | day | week | month | year | [optional][default to &#39;&#39;] |
| **page** | **Integer** | 30 results per page | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## duckduckgo_search_suggestions

> Object duckduckgo_search_suggestions(query, opts)

Search suggestions

DuckDuckGo search-box suggestions.

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

api_instance = ScrapeBadger::DuckDuckGoApi.new
query = 'query_example' # String | Partial query to complete
opts = {
  region: 'region_example' # String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
}

begin
  # Search suggestions
  result = api_instance.duckduckgo_search_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_search_suggestions: #{e}"
end
```

#### Using the duckduckgo_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> duckduckgo_search_suggestions_with_http_info(query, opts)

```ruby
begin
  # Search suggestions
  data, status_code, headers = api_instance.duckduckgo_search_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial query to complete |  |
| **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional][default to &#39;wt-wt&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## duckduckgo_video_search

> Object duckduckgo_video_search(query, opts)

Video search

DuckDuckGo video search — title, publisher, uploader, duration, views, thumbnails.

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

api_instance = ScrapeBadger::DuckDuckGoApi.new
query = 'query_example' # String | Search query
opts = {
  region: 'region_example', # String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
  safesearch: 'safesearch_example', # String | on | moderate | off
  page: 56, # Integer | 60 results per page
  duration: 'duration_example', # String | short | medium | long
  resolution: 'resolution_example' # String | high | standard
}

begin
  # Video search
  result = api_instance.duckduckgo_video_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_video_search: #{e}"
end
```

#### Using the duckduckgo_video_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> duckduckgo_video_search_with_http_info(query, opts)

```ruby
begin
  # Video search
  data, status_code, headers = api_instance.duckduckgo_video_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_video_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search query |  |
| **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional][default to &#39;wt-wt&#39;] |
| **safesearch** | **String** | on | moderate | off | [optional][default to &#39;moderate&#39;] |
| **page** | **Integer** | 60 results per page | [optional][default to 1] |
| **duration** | **String** | short | medium | long | [optional][default to &#39;&#39;] |
| **resolution** | **String** | high | standard | [optional][default to &#39;&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## duckduckgo_web_search

> Object duckduckgo_web_search(query, opts)

Web search

DuckDuckGo web SERP — organic results, the zero-click abstract box, ads flagged.

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

api_instance = ScrapeBadger::DuckDuckGoApi.new
query = 'query_example' # String | Search query
opts = {
  region: 'region_example', # String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
  safesearch: 'safesearch_example', # String | on | moderate | off
  timelimit: 'timelimit_example', # String | day | week | month | year
  page: 56 # Integer | 
}

begin
  # Web search
  result = api_instance.duckduckgo_web_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_web_search: #{e}"
end
```

#### Using the duckduckgo_web_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> duckduckgo_web_search_with_http_info(query, opts)

```ruby
begin
  # Web search
  data, status_code, headers = api_instance.duckduckgo_web_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DuckDuckGoApi->duckduckgo_web_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search query |  |
| **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional][default to &#39;wt-wt&#39;] |
| **safesearch** | **String** | on | moderate | off | [optional][default to &#39;moderate&#39;] |
| **timelimit** | **String** | day | week | month | year | [optional][default to &#39;&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

