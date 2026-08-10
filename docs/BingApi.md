# ScrapeBadger::BingApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**bing_bing_scraper_health_check**](BingApi.md#bing_bing_scraper_health_check) | **GET** /v1/bing/health | Bing scraper health check |
| [**bing_bing_scraper_health_check_head**](BingApi.md#bing_bing_scraper_health_check_head) | **HEAD** /v1/bing/health | Bing scraper health check |
| [**bing_image_search**](BingApi.md#bing_image_search) | **GET** /v1/bing/images | Image search |
| [**bing_list_supported_markets**](BingApi.md#bing_list_supported_markets) | **GET** /v1/bing/markets | List supported markets |
| [**bing_news_search**](BingApi.md#bing_news_search) | **GET** /v1/bing/news | News search |
| [**bing_search_suggestions**](BingApi.md#bing_search_suggestions) | **GET** /v1/bing/autocomplete | Search suggestions |
| [**bing_video_search**](BingApi.md#bing_video_search) | **GET** /v1/bing/videos | Video search |
| [**bing_web_search**](BingApi.md#bing_web_search) | **GET** /v1/bing/search | Web search |


## bing_bing_scraper_health_check

> Object bing_bing_scraper_health_check

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::BingApi.new

begin
  # Bing scraper health check
  result = api_instance.bing_bing_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_bing_scraper_health_check: #{e}"
end
```

#### Using the bing_bing_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bing_bing_scraper_health_check_with_http_info

```ruby
begin
  # Bing scraper health check
  data, status_code, headers = api_instance.bing_bing_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_bing_scraper_health_check_with_http_info: #{e}"
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


## bing_bing_scraper_health_check_head

> Object bing_bing_scraper_health_check_head

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::BingApi.new

begin
  # Bing scraper health check
  result = api_instance.bing_bing_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_bing_scraper_health_check_head: #{e}"
end
```

#### Using the bing_bing_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bing_bing_scraper_health_check_head_with_http_info

```ruby
begin
  # Bing scraper health check
  data, status_code, headers = api_instance.bing_bing_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_bing_scraper_health_check_head_with_http_info: #{e}"
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


## bing_image_search

> Object bing_image_search(query, opts)

Image search

Bing Images — thumbnail, full-size and source URL per result.

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

api_instance = ScrapeBadger::BingApi.new
query = 'query_example' # String | Search keywords, e.g. 'golden retriever'
opts = {
  market: 'market_example', # String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
  count: 56, # Integer | Results to return
  safe_search: 'safe_search_example' # String | off | moderate | strict
}

begin
  # Image search
  result = api_instance.bing_image_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_image_search: #{e}"
end
```

#### Using the bing_image_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bing_image_search_with_http_info(query, opts)

```ruby
begin
  # Image search
  data, status_code, headers = api_instance.bing_image_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_image_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;golden retriever&#39; |  |
| **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional][default to &#39;en-US&#39;] |
| **count** | **Integer** | Results to return | [optional][default to 35] |
| **safe_search** | **String** | off | moderate | strict | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bing_list_supported_markets

> Object bing_list_supported_markets

List supported markets

Supported Bing market codes. Free — costs no credits.

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

api_instance = ScrapeBadger::BingApi.new

begin
  # List supported markets
  result = api_instance.bing_list_supported_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_list_supported_markets: #{e}"
end
```

#### Using the bing_list_supported_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bing_list_supported_markets_with_http_info

```ruby
begin
  # List supported markets
  data, status_code, headers = api_instance.bing_list_supported_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_list_supported_markets_with_http_info: #{e}"
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


## bing_news_search

> Object bing_news_search(query, opts)

News search

Bing News — headline, source, published time and snippet per article.

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

api_instance = ScrapeBadger::BingApi.new
query = 'query_example' # String | Search keywords, e.g. 'interest rates'
opts = {
  market: 'market_example', # String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
  freshness: 'freshness_example' # String | day | week | month — restrict to recent articles
}

begin
  # News search
  result = api_instance.bing_news_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_news_search: #{e}"
end
```

#### Using the bing_news_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bing_news_search_with_http_info(query, opts)

```ruby
begin
  # News search
  data, status_code, headers = api_instance.bing_news_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_news_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;interest rates&#39; |  |
| **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional][default to &#39;en-US&#39;] |
| **freshness** | **String** | day | week | month — restrict to recent articles | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bing_search_suggestions

> Object bing_search_suggestions(query, opts)

Search suggestions

Bing search-box query suggestions.

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

api_instance = ScrapeBadger::BingApi.new
query = 'query_example' # String | Partial search term, e.g. 'coff'
opts = {
  market: 'market_example' # String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
}

begin
  # Search suggestions
  result = api_instance.bing_search_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_search_suggestions: #{e}"
end
```

#### Using the bing_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bing_search_suggestions_with_http_info(query, opts)

```ruby
begin
  # Search suggestions
  data, status_code, headers = api_instance.bing_search_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial search term, e.g. &#39;coff&#39; |  |
| **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional][default to &#39;en-US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bing_video_search

> Object bing_video_search(query, opts)

Video search

Bing Videos — title, thumbnail, duration, publisher and source per result.

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

api_instance = ScrapeBadger::BingApi.new
query = 'query_example' # String | Search keywords, e.g. 'espresso tutorial'
opts = {
  market: 'market_example', # String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
  count: 56, # Integer | Results to return
  safe_search: 'safe_search_example' # String | off | moderate | strict
}

begin
  # Video search
  result = api_instance.bing_video_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_video_search: #{e}"
end
```

#### Using the bing_video_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bing_video_search_with_http_info(query, opts)

```ruby
begin
  # Video search
  data, status_code, headers = api_instance.bing_video_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_video_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;espresso tutorial&#39; |  |
| **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional][default to &#39;en-US&#39;] |
| **count** | **Integer** | Results to return | [optional][default to 35] |
| **safe_search** | **String** | off | moderate | strict | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bing_web_search

> Object bing_web_search(query, opts)

Web search

Bing web SERP — organic results, ads, related searches and total count.

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

api_instance = ScrapeBadger::BingApi.new
query = 'query_example' # String | Search keywords, e.g. 'coffee machine'
opts = {
  market: 'market_example', # String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
  count: 56, # Integer | Results per page (1-50)
  offset: 56, # Integer | Zero-based result offset for pagination
  safe_search: 'safe_search_example' # String | off | moderate | strict (default moderate)
}

begin
  # Web search
  result = api_instance.bing_web_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_web_search: #{e}"
end
```

#### Using the bing_web_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> bing_web_search_with_http_info(query, opts)

```ruby
begin
  # Web search
  data, status_code, headers = api_instance.bing_web_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BingApi->bing_web_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;coffee machine&#39; |  |
| **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional][default to &#39;en-US&#39;] |
| **count** | **Integer** | Results per page (1-50) | [optional][default to 10] |
| **offset** | **Integer** | Zero-based result offset for pagination | [optional][default to 0] |
| **safe_search** | **String** | off | moderate | strict (default moderate) | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

