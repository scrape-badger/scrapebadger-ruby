# ScrapeBadger::GrokApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**grok_ask_grok_a_question**](GrokApi.md#grok_ask_grok_a_question) | **GET** /v1/grok/ask | Ask Grok a question |
| [**grok_ask_grok_a_question_post**](GrokApi.md#grok_ask_grok_a_question_post) | **POST** /v1/grok/ask | Ask Grok a question (POST) |
| [**grok_get_a_grok_conversation**](GrokApi.md#grok_get_a_grok_conversation) | **GET** /v1/grok/conversations/{conversation_id} | Get a Grok conversation |
| [**grok_grok_scraper_health_check**](GrokApi.md#grok_grok_scraper_health_check) | **GET** /v1/grok/health | Grok scraper health check |
| [**grok_grok_scraper_health_check_head**](GrokApi.md#grok_grok_scraper_health_check_head) | **HEAD** /v1/grok/health | Grok scraper health check |
| [**grok_list_grok_assistant_modes**](GrokApi.md#grok_list_grok_assistant_modes) | **GET** /v1/grok/models | List Grok assistant modes |
| [**grok_measure_brand_visibility_in_grok**](GrokApi.md#grok_measure_brand_visibility_in_grok) | **GET** /v1/grok/brand-visibility | Measure brand visibility in Grok |
| [**grok_measure_brand_visibility_in_grok_post**](GrokApi.md#grok_measure_brand_visibility_in_grok_post) | **POST** /v1/grok/brand-visibility | Measure brand visibility in Grok (POST) |


## grok_ask_grok_a_question

> Object grok_ask_grok_a_question(prompt, opts)

Ask Grok a question

Ask the real Grok assistant and get its answer, web sources, and X post references.

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

api_instance = ScrapeBadger::GrokApi.new
prompt = 'prompt_example' # String | Prompt to send to Grok (max 4000 characters).
opts = {
  conversation_id: 'conversation_id_example', # String | Existing Grok conversation to continue.
  mode: 'mode_example', # String | Assistant mode: auto, fast, or expert.
  web_search: 'web_search_example' # String | Web and X search: auto, force, or off.
}

begin
  # Ask Grok a question
  result = api_instance.grok_ask_grok_a_question(prompt, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_ask_grok_a_question: #{e}"
end
```

#### Using the grok_ask_grok_a_question_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_ask_grok_a_question_with_http_info(prompt, opts)

```ruby
begin
  # Ask Grok a question
  data, status_code, headers = api_instance.grok_ask_grok_a_question_with_http_info(prompt, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_ask_grok_a_question_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | Prompt to send to Grok (max 4000 characters). |  |
| **conversation_id** | **String** | Existing Grok conversation to continue. | [optional] |
| **mode** | **String** | Assistant mode: auto, fast, or expert. | [optional][default to &#39;auto&#39;] |
| **web_search** | **String** | Web and X search: auto, force, or off. | [optional][default to &#39;auto&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## grok_ask_grok_a_question_post

> Object grok_ask_grok_a_question_post

Ask Grok a question (POST)

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

api_instance = ScrapeBadger::GrokApi.new

begin
  # Ask Grok a question (POST)
  result = api_instance.grok_ask_grok_a_question_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_ask_grok_a_question_post: #{e}"
end
```

#### Using the grok_ask_grok_a_question_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_ask_grok_a_question_post_with_http_info

```ruby
begin
  # Ask Grok a question (POST)
  data, status_code, headers = api_instance.grok_ask_grok_a_question_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_ask_grok_a_question_post_with_http_info: #{e}"
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


## grok_get_a_grok_conversation

> Object grok_get_a_grok_conversation(conversation_id)

Get a Grok conversation

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

api_instance = ScrapeBadger::GrokApi.new
conversation_id = 'conversation_id_example' # String | 

begin
  # Get a Grok conversation
  result = api_instance.grok_get_a_grok_conversation(conversation_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_get_a_grok_conversation: #{e}"
end
```

#### Using the grok_get_a_grok_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_get_a_grok_conversation_with_http_info(conversation_id)

```ruby
begin
  # Get a Grok conversation
  data, status_code, headers = api_instance.grok_get_a_grok_conversation_with_http_info(conversation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_get_a_grok_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **conversation_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## grok_grok_scraper_health_check

> Object grok_grok_scraper_health_check

Grok scraper health check

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

api_instance = ScrapeBadger::GrokApi.new

begin
  # Grok scraper health check
  result = api_instance.grok_grok_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_grok_scraper_health_check: #{e}"
end
```

#### Using the grok_grok_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_grok_scraper_health_check_with_http_info

```ruby
begin
  # Grok scraper health check
  data, status_code, headers = api_instance.grok_grok_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_grok_scraper_health_check_with_http_info: #{e}"
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


## grok_grok_scraper_health_check_head

> Object grok_grok_scraper_health_check_head

Grok scraper health check

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

api_instance = ScrapeBadger::GrokApi.new

begin
  # Grok scraper health check
  result = api_instance.grok_grok_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_grok_scraper_health_check_head: #{e}"
end
```

#### Using the grok_grok_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_grok_scraper_health_check_head_with_http_info

```ruby
begin
  # Grok scraper health check
  data, status_code, headers = api_instance.grok_grok_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_grok_scraper_health_check_head_with_http_info: #{e}"
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


## grok_list_grok_assistant_modes

> Object grok_list_grok_assistant_modes

List Grok assistant modes

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

api_instance = ScrapeBadger::GrokApi.new

begin
  # List Grok assistant modes
  result = api_instance.grok_list_grok_assistant_modes
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_list_grok_assistant_modes: #{e}"
end
```

#### Using the grok_list_grok_assistant_modes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_list_grok_assistant_modes_with_http_info

```ruby
begin
  # List Grok assistant modes
  data, status_code, headers = api_instance.grok_list_grok_assistant_modes_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_list_grok_assistant_modes_with_http_info: #{e}"
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


## grok_measure_brand_visibility_in_grok

> Object grok_measure_brand_visibility_in_grok(prompt, brand, opts)

Measure brand visibility in Grok

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

api_instance = ScrapeBadger::GrokApi.new
prompt = 'prompt_example' # String | Buyer or category prompt to send to Grok.
brand = 'brand_example' # String | Brand name to measure.
opts = {
  competitors: ['inner_example'], # Array<String> | Competitor brand names.
  brand_domain: 'brand_domain_example', # String | Brand domain for citation rank.
  mode: 'mode_example', # String | Assistant mode: auto, fast, or expert.
  web_search: 'web_search_example' # String | Web and X search mode.
}

begin
  # Measure brand visibility in Grok
  result = api_instance.grok_measure_brand_visibility_in_grok(prompt, brand, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_measure_brand_visibility_in_grok: #{e}"
end
```

#### Using the grok_measure_brand_visibility_in_grok_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_measure_brand_visibility_in_grok_with_http_info(prompt, brand, opts)

```ruby
begin
  # Measure brand visibility in Grok
  data, status_code, headers = api_instance.grok_measure_brand_visibility_in_grok_with_http_info(prompt, brand, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_measure_brand_visibility_in_grok_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | Buyer or category prompt to send to Grok. |  |
| **brand** | **String** | Brand name to measure. |  |
| **competitors** | [**Array&lt;String&gt;**](String.md) | Competitor brand names. | [optional] |
| **brand_domain** | **String** | Brand domain for citation rank. | [optional] |
| **mode** | **String** | Assistant mode: auto, fast, or expert. | [optional][default to &#39;auto&#39;] |
| **web_search** | **String** | Web and X search mode. | [optional][default to &#39;force&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## grok_measure_brand_visibility_in_grok_post

> Object grok_measure_brand_visibility_in_grok_post

Measure brand visibility in Grok (POST)

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

api_instance = ScrapeBadger::GrokApi.new

begin
  # Measure brand visibility in Grok (POST)
  result = api_instance.grok_measure_brand_visibility_in_grok_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_measure_brand_visibility_in_grok_post: #{e}"
end
```

#### Using the grok_measure_brand_visibility_in_grok_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_measure_brand_visibility_in_grok_post_with_http_info

```ruby
begin
  # Measure brand visibility in Grok (POST)
  data, status_code, headers = api_instance.grok_measure_brand_visibility_in_grok_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_measure_brand_visibility_in_grok_post_with_http_info: #{e}"
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

