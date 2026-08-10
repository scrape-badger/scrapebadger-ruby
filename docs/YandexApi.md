# ScrapeBadger::YandexApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**yandex_image_search**](YandexApi.md#yandex_image_search) | **GET** /v1/yandex/images/search | Image search |
| [**yandex_list_supported_markets**](YandexApi.md#yandex_list_supported_markets) | **GET** /v1/yandex/markets | List supported markets |
| [**yandex_reverse_image_search**](YandexApi.md#yandex_reverse_image_search) | **GET** /v1/yandex/images/reverse | Reverse image search |
| [**yandex_web_search**](YandexApi.md#yandex_web_search) | **GET** /v1/yandex/search | Web search |
| [**yandex_yandex_scraper_health_check**](YandexApi.md#yandex_yandex_scraper_health_check) | **GET** /v1/yandex/health | Yandex scraper health check |
| [**yandex_yandex_scraper_health_check_head**](YandexApi.md#yandex_yandex_scraper_health_check_head) | **HEAD** /v1/yandex/health | Yandex scraper health check |


## yandex_image_search

> Object yandex_image_search(query, opts)

Image search

Search Yandex Images by text — thumbnail, full-res URL, dimensions, source page.

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

api_instance = ScrapeBadger::YandexApi.new
query = 'query_example' # String | Image search query, e.g. 'coffee machine'
opts = {
  domain: 'domain_example', # String | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate.
  page: 56 # Integer | 
}

begin
  # Image search
  result = api_instance.yandex_image_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_image_search: #{e}"
end
```

#### Using the yandex_image_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yandex_image_search_with_http_info(query, opts)

```ruby
begin
  # Image search
  data, status_code, headers = api_instance.yandex_image_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_image_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Image search query, e.g. &#39;coffee machine&#39; |  |
| **domain** | **String** | Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional][default to &#39;tr&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## yandex_list_supported_markets

> Object yandex_list_supported_markets

List supported markets

Supported Yandex markets (domains, default region and language).

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

api_instance = ScrapeBadger::YandexApi.new

begin
  # List supported markets
  result = api_instance.yandex_list_supported_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_list_supported_markets: #{e}"
end
```

#### Using the yandex_list_supported_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yandex_list_supported_markets_with_http_info

```ruby
begin
  # List supported markets
  data, status_code, headers = api_instance.yandex_list_supported_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_list_supported_markets_with_http_info: #{e}"
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


## yandex_reverse_image_search

> Object yandex_reverse_image_search(image_url, opts)

Reverse image search

Reverse image search by URL — hosting pages, similar images, tags, other sizes.

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

api_instance = ScrapeBadger::YandexApi.new
image_url = 'image_url_example' # String | Public URL of the image to reverse-search
opts = {
  domain: 'domain_example' # String | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate.
}

begin
  # Reverse image search
  result = api_instance.yandex_reverse_image_search(image_url, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_reverse_image_search: #{e}"
end
```

#### Using the yandex_reverse_image_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yandex_reverse_image_search_with_http_info(image_url, opts)

```ruby
begin
  # Reverse image search
  data, status_code, headers = api_instance.yandex_reverse_image_search_with_http_info(image_url, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_reverse_image_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **image_url** | **String** | Public URL of the image to reverse-search |  |
| **domain** | **String** | Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional][default to &#39;tr&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## yandex_web_search

> Object yandex_web_search(query, opts)

Web search

Search Yandex web results — organic results, ads, displayed URLs, snippets.

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

api_instance = ScrapeBadger::YandexApi.new
query = 'query_example' # String | Search query, e.g. 'coffee machine'
opts = {
  domain: 'domain_example', # String | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate.
  page: 56, # Integer | 
  lr: 56, # Integer | Yandex region id, e.g. 213=Moscow, 84=USA
  lang: 'lang_example' # String | UI language: ru, en, tr, be, kk, uk
}

begin
  # Web search
  result = api_instance.yandex_web_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_web_search: #{e}"
end
```

#### Using the yandex_web_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yandex_web_search_with_http_info(query, opts)

```ruby
begin
  # Web search
  data, status_code, headers = api_instance.yandex_web_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_web_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search query, e.g. &#39;coffee machine&#39; |  |
| **domain** | **String** | Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional][default to &#39;tr&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **lr** | **Integer** | Yandex region id, e.g. 213&#x3D;Moscow, 84&#x3D;USA | [optional] |
| **lang** | **String** | UI language: ru, en, tr, be, kk, uk | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## yandex_yandex_scraper_health_check

> Object yandex_yandex_scraper_health_check

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::YandexApi.new

begin
  # Yandex scraper health check
  result = api_instance.yandex_yandex_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_yandex_scraper_health_check: #{e}"
end
```

#### Using the yandex_yandex_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yandex_yandex_scraper_health_check_with_http_info

```ruby
begin
  # Yandex scraper health check
  data, status_code, headers = api_instance.yandex_yandex_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_yandex_scraper_health_check_with_http_info: #{e}"
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


## yandex_yandex_scraper_health_check_head

> Object yandex_yandex_scraper_health_check_head

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::YandexApi.new

begin
  # Yandex scraper health check
  result = api_instance.yandex_yandex_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_yandex_scraper_health_check_head: #{e}"
end
```

#### Using the yandex_yandex_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> yandex_yandex_scraper_health_check_head_with_http_info

```ruby
begin
  # Yandex scraper health check
  data, status_code, headers = api_instance.yandex_yandex_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YandexApi->yandex_yandex_scraper_health_check_head_with_http_info: #{e}"
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

