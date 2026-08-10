# ScrapeBadger::BaiduApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**baidu_baidu_image_search**](BaiduApi.md#baidu_baidu_image_search) | **GET** /v1/baidu/images | Baidu image search |
| [**baidu_baidu_news_search**](BaiduApi.md#baidu_baidu_news_search) | **GET** /v1/baidu/news | Baidu news search |
| [**baidu_baidu_scraper_health_check**](BaiduApi.md#baidu_baidu_scraper_health_check) | **GET** /v1/baidu/health | Baidu scraper health check |
| [**baidu_baidu_scraper_health_check_head**](BaiduApi.md#baidu_baidu_scraper_health_check_head) | **HEAD** /v1/baidu/health | Baidu scraper health check |
| [**baidu_baidu_web_search**](BaiduApi.md#baidu_baidu_web_search) | **GET** /v1/baidu/search | Baidu web search |
| [**baidu_search_suggestions**](BaiduApi.md#baidu_search_suggestions) | **GET** /v1/baidu/autocomplete | Search suggestions |


## baidu_baidu_image_search

> Object baidu_baidu_image_search(query, opts)

Baidu image search

Baidu image search via the acjson JSON API.

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

api_instance = ScrapeBadger::BaiduApi.new
query = 'query_example' # String | Search keywords
opts = {
  page: 56 # Integer | 30 images per page
}

begin
  # Baidu image search
  result = api_instance.baidu_baidu_image_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_image_search: #{e}"
end
```

#### Using the baidu_baidu_image_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> baidu_baidu_image_search_with_http_info(query, opts)

```ruby
begin
  # Baidu image search
  data, status_code, headers = api_instance.baidu_baidu_image_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_image_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords |  |
| **page** | **Integer** | 30 images per page | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## baidu_baidu_news_search

> Object baidu_baidu_news_search(query, opts)

Baidu news search

Baidu news vertical — articles with source, publish date and real URLs.

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

api_instance = ScrapeBadger::BaiduApi.new
query = 'query_example' # String | Search keywords
opts = {
  page: 56 # Integer | 
}

begin
  # Baidu news search
  result = api_instance.baidu_baidu_news_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_news_search: #{e}"
end
```

#### Using the baidu_baidu_news_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> baidu_baidu_news_search_with_http_info(query, opts)

```ruby
begin
  # Baidu news search
  data, status_code, headers = api_instance.baidu_baidu_news_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_news_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords |  |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## baidu_baidu_scraper_health_check

> Object baidu_baidu_scraper_health_check

Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::BaiduApi.new

begin
  # Baidu scraper health check
  result = api_instance.baidu_baidu_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_scraper_health_check: #{e}"
end
```

#### Using the baidu_baidu_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> baidu_baidu_scraper_health_check_with_http_info

```ruby
begin
  # Baidu scraper health check
  data, status_code, headers = api_instance.baidu_baidu_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_scraper_health_check_with_http_info: #{e}"
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


## baidu_baidu_scraper_health_check_head

> Object baidu_baidu_scraper_health_check_head

Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::BaiduApi.new

begin
  # Baidu scraper health check
  result = api_instance.baidu_baidu_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_scraper_health_check_head: #{e}"
end
```

#### Using the baidu_baidu_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> baidu_baidu_scraper_health_check_head_with_http_info

```ruby
begin
  # Baidu scraper health check
  data, status_code, headers = api_instance.baidu_baidu_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_scraper_health_check_head_with_http_info: #{e}"
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


## baidu_baidu_web_search

> Object baidu_baidu_web_search(query, opts)

Baidu web search

Baidu web SERP — organic results with real target URLs, related searches, total count.

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

api_instance = ScrapeBadger::BaiduApi.new
query = 'query_example' # String | Search keywords, e.g. '咖啡机' or 'coffee machine'
opts = {
  page: 56, # Integer | Result page (10 results per page)
  num: 56 # Integer | Results per page (rn)
}

begin
  # Baidu web search
  result = api_instance.baidu_baidu_web_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_web_search: #{e}"
end
```

#### Using the baidu_baidu_web_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> baidu_baidu_web_search_with_http_info(query, opts)

```ruby
begin
  # Baidu web search
  data, status_code, headers = api_instance.baidu_baidu_web_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_baidu_web_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;咖啡机&#39; or &#39;coffee machine&#39; |  |
| **page** | **Integer** | Result page (10 results per page) | [optional][default to 1] |
| **num** | **Integer** | Results per page (rn) | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## baidu_search_suggestions

> Object baidu_search_suggestions(query)

Search suggestions

Baidu search-box suggestions.

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

api_instance = ScrapeBadger::BaiduApi.new
query = 'query_example' # String | Partial search term, e.g. '咖啡' or 'coff'

begin
  # Search suggestions
  result = api_instance.baidu_search_suggestions(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_search_suggestions: #{e}"
end
```

#### Using the baidu_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> baidu_search_suggestions_with_http_info(query)

```ruby
begin
  # Search suggestions
  data, status_code, headers = api_instance.baidu_search_suggestions_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BaiduApi->baidu_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial search term, e.g. &#39;咖啡&#39; or &#39;coff&#39; |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

