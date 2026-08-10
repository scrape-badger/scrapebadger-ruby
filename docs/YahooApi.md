# ScrapeBadger::YahooApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**yahoo_image_search**](YahooApi.md#yahoo_image_search) | **GET** /v1/yahoo/images | Image search |
| [**yahoo_list_supported_markets**](YahooApi.md#yahoo_list_supported_markets) | **GET** /v1/yahoo/markets | List supported markets |
| [**yahoo_news_search**](YahooApi.md#yahoo_news_search) | **GET** /v1/yahoo/news | News search |
| [**yahoo_search_suggestions**](YahooApi.md#yahoo_search_suggestions) | **GET** /v1/yahoo/autocomplete | Search suggestions |
| [**yahoo_video_search**](YahooApi.md#yahoo_video_search) | **GET** /v1/yahoo/videos | Video search |
| [**yahoo_web_search**](YahooApi.md#yahoo_web_search) | **GET** /v1/yahoo/search | Web search |
| [**yahoo_yahoo_scraper_health_check**](YahooApi.md#yahoo_yahoo_scraper_health_check) | **GET** /v1/yahoo/health | Yahoo scraper health check |
| [**yahoo_yahoo_scraper_health_check_head**](YahooApi.md#yahoo_yahoo_scraper_health_check_head) | **HEAD** /v1/yahoo/health | Yahoo scraper health check |


## yahoo_image_search

> Object yahoo_image_search(query, opts)

Image search

Yahoo Images — thumbnail, full-size and source URL per result.

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

api_instance = ScrapeBadger::YahooApi.new
query = 'query_example' # String | Search keywords, e.g. 'golden retriever'
opts = {
  market: 'market_example', # String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
  count: 56 # Integer | Results to return
}

begin
  # Image search
  result = api_instance.yahoo_image_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_image_search: #{e}"
end
```

#### Using the yahoo_image_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yahoo_image_search_with_http_info(query, opts)

```ruby
begin
  # Image search
  data, status_code, headers = api_instance.yahoo_image_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_image_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;golden retriever&#39; |  |
| **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional][default to &#39;us&#39;] |
| **count** | **Integer** | Results to return | [optional][default to 30] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## yahoo_list_supported_markets

> Object yahoo_list_supported_markets

List supported markets

Supported Yahoo market codes. Free — costs no credits.

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

api_instance = ScrapeBadger::YahooApi.new

begin
  # List supported markets
  result = api_instance.yahoo_list_supported_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_list_supported_markets: #{e}"
end
```

#### Using the yahoo_list_supported_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yahoo_list_supported_markets_with_http_info

```ruby
begin
  # List supported markets
  data, status_code, headers = api_instance.yahoo_list_supported_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_list_supported_markets_with_http_info: #{e}"
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


## yahoo_news_search

> Object yahoo_news_search(query, opts)

News search

Yahoo News — headline, source, published time and snippet per article.

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

api_instance = ScrapeBadger::YahooApi.new
query = 'query_example' # String | Search keywords, e.g. 'interest rates'
opts = {
  market: 'market_example' # String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
}

begin
  # News search
  result = api_instance.yahoo_news_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_news_search: #{e}"
end
```

#### Using the yahoo_news_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yahoo_news_search_with_http_info(query, opts)

```ruby
begin
  # News search
  data, status_code, headers = api_instance.yahoo_news_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_news_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;interest rates&#39; |  |
| **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## yahoo_search_suggestions

> Object yahoo_search_suggestions(query, opts)

Search suggestions

Yahoo search-box query suggestions.

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

api_instance = ScrapeBadger::YahooApi.new
query = 'query_example' # String | Partial search term, e.g. 'coff'
opts = {
  market: 'market_example' # String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
}

begin
  # Search suggestions
  result = api_instance.yahoo_search_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_search_suggestions: #{e}"
end
```

#### Using the yahoo_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yahoo_search_suggestions_with_http_info(query, opts)

```ruby
begin
  # Search suggestions
  data, status_code, headers = api_instance.yahoo_search_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial search term, e.g. &#39;coff&#39; |  |
| **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## yahoo_video_search

> Object yahoo_video_search(query, opts)

Video search

Yahoo Videos — title, thumbnail, duration, publisher and source per result.

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

api_instance = ScrapeBadger::YahooApi.new
query = 'query_example' # String | Search keywords, e.g. 'espresso tutorial'
opts = {
  market: 'market_example', # String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
  count: 56 # Integer | Results to return
}

begin
  # Video search
  result = api_instance.yahoo_video_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_video_search: #{e}"
end
```

#### Using the yahoo_video_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yahoo_video_search_with_http_info(query, opts)

```ruby
begin
  # Video search
  data, status_code, headers = api_instance.yahoo_video_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_video_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;espresso tutorial&#39; |  |
| **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional][default to &#39;us&#39;] |
| **count** | **Integer** | Results to return | [optional][default to 30] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## yahoo_web_search

> Object yahoo_web_search(query, opts)

Web search

Yahoo web SERP — organic results, ads, related searches and total count.

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

api_instance = ScrapeBadger::YahooApi.new
query = 'query_example' # String | Search keywords, e.g. 'coffee machine'
opts = {
  market: 'market_example', # String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
  offset: 56, # Integer | Zero-based result offset for pagination
  safe_search: 'safe_search_example' # String | off | moderate | strict (default moderate)
}

begin
  # Web search
  result = api_instance.yahoo_web_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_web_search: #{e}"
end
```

#### Using the yahoo_web_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yahoo_web_search_with_http_info(query, opts)

```ruby
begin
  # Web search
  data, status_code, headers = api_instance.yahoo_web_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_web_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;coffee machine&#39; |  |
| **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional][default to &#39;us&#39;] |
| **offset** | **Integer** | Zero-based result offset for pagination | [optional][default to 0] |
| **safe_search** | **String** | off | moderate | strict (default moderate) | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## yahoo_yahoo_scraper_health_check

> Object yahoo_yahoo_scraper_health_check

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::YahooApi.new

begin
  # Yahoo scraper health check
  result = api_instance.yahoo_yahoo_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_yahoo_scraper_health_check: #{e}"
end
```

#### Using the yahoo_yahoo_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yahoo_yahoo_scraper_health_check_with_http_info

```ruby
begin
  # Yahoo scraper health check
  data, status_code, headers = api_instance.yahoo_yahoo_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_yahoo_scraper_health_check_with_http_info: #{e}"
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


## yahoo_yahoo_scraper_health_check_head

> Object yahoo_yahoo_scraper_health_check_head

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::YahooApi.new

begin
  # Yahoo scraper health check
  result = api_instance.yahoo_yahoo_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_yahoo_scraper_health_check_head: #{e}"
end
```

#### Using the yahoo_yahoo_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yahoo_yahoo_scraper_health_check_head_with_http_info

```ruby
begin
  # Yahoo scraper health check
  data, status_code, headers = api_instance.yahoo_yahoo_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YahooApi->yahoo_yahoo_scraper_health_check_head_with_http_info: #{e}"
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

