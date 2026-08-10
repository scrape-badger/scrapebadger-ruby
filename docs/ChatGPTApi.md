# ScrapeBadger::ChatGPTApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**chatgpt_ask_chatgpt_a_question**](ChatGPTApi.md#chatgpt_ask_chatgpt_a_question) | **GET** /v1/chatgpt/ask | Ask ChatGPT a question |
| [**chatgpt_ask_chatgpt_a_question_post**](ChatGPTApi.md#chatgpt_ask_chatgpt_a_question_post) | **POST** /v1/chatgpt/ask | Ask ChatGPT a question (POST) |
| [**chatgpt_chatgpt_scraper_health_check**](ChatGPTApi.md#chatgpt_chatgpt_scraper_health_check) | **GET** /v1/chatgpt/health | ChatGPT scraper health check |
| [**chatgpt_chatgpt_scraper_health_check_head**](ChatGPTApi.md#chatgpt_chatgpt_scraper_health_check_head) | **HEAD** /v1/chatgpt/health | ChatGPT scraper health check |
| [**chatgpt_list_chatgpt_models**](ChatGPTApi.md#chatgpt_list_chatgpt_models) | **GET** /v1/chatgpt/models | List ChatGPT models |
| [**chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer**](ChatGPTApi.md#chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer) | **GET** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer |
| [**chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post**](ChatGPTApi.md#chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post) | **POST** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer (POST) |


## chatgpt_ask_chatgpt_a_question

> Object chatgpt_ask_chatgpt_a_question(prompt, opts)

Ask ChatGPT a question

Send a prompt to ChatGPT and get the answer plus the web sources it cited.

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

api_instance = ScrapeBadger::ChatGPTApi.new
prompt = 'prompt_example' # String | The prompt to send to ChatGPT (max 4096 characters).
opts = {
  country: 'country_example', # String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
  web_search: 'web_search_example' # String | auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened.
}

begin
  # Ask ChatGPT a question
  result = api_instance.chatgpt_ask_chatgpt_a_question(prompt, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_ask_chatgpt_a_question: #{e}"
end
```

#### Using the chatgpt_ask_chatgpt_a_question_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> chatgpt_ask_chatgpt_a_question_with_http_info(prompt, opts)

```ruby
begin
  # Ask ChatGPT a question
  data, status_code, headers = api_instance.chatgpt_ask_chatgpt_a_question_with_http_info(prompt, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_ask_chatgpt_a_question_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The prompt to send to ChatGPT (max 4096 characters). |  |
| **country** | **String** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |
| **web_search** | **String** | auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional][default to &#39;auto&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## chatgpt_ask_chatgpt_a_question_post

> Object chatgpt_ask_chatgpt_a_question_post

Ask ChatGPT a question (POST)

POST form of `/ask`, for prompts too long for a query string.

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

api_instance = ScrapeBadger::ChatGPTApi.new

begin
  # Ask ChatGPT a question (POST)
  result = api_instance.chatgpt_ask_chatgpt_a_question_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_ask_chatgpt_a_question_post: #{e}"
end
```

#### Using the chatgpt_ask_chatgpt_a_question_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> chatgpt_ask_chatgpt_a_question_post_with_http_info

```ruby
begin
  # Ask ChatGPT a question (POST)
  data, status_code, headers = api_instance.chatgpt_ask_chatgpt_a_question_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_ask_chatgpt_a_question_post_with_http_info: #{e}"
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


## chatgpt_chatgpt_scraper_health_check

> Object chatgpt_chatgpt_scraper_health_check

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::ChatGPTApi.new

begin
  # ChatGPT scraper health check
  result = api_instance.chatgpt_chatgpt_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_chatgpt_scraper_health_check: #{e}"
end
```

#### Using the chatgpt_chatgpt_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> chatgpt_chatgpt_scraper_health_check_with_http_info

```ruby
begin
  # ChatGPT scraper health check
  data, status_code, headers = api_instance.chatgpt_chatgpt_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_chatgpt_scraper_health_check_with_http_info: #{e}"
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


## chatgpt_chatgpt_scraper_health_check_head

> Object chatgpt_chatgpt_scraper_health_check_head

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::ChatGPTApi.new

begin
  # ChatGPT scraper health check
  result = api_instance.chatgpt_chatgpt_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_chatgpt_scraper_health_check_head: #{e}"
end
```

#### Using the chatgpt_chatgpt_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> chatgpt_chatgpt_scraper_health_check_head_with_http_info

```ruby
begin
  # ChatGPT scraper health check
  data, status_code, headers = api_instance.chatgpt_chatgpt_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_chatgpt_scraper_health_check_head_with_http_info: #{e}"
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


## chatgpt_list_chatgpt_models

> Object chatgpt_list_chatgpt_models(opts)

List ChatGPT models

Models chatgpt.com currently serves to an anonymous visitor.

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

api_instance = ScrapeBadger::ChatGPTApi.new
opts = {
  country: 'country_example' # String | ISO-3166 alpha-2 egress country.
}

begin
  # List ChatGPT models
  result = api_instance.chatgpt_list_chatgpt_models(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_list_chatgpt_models: #{e}"
end
```

#### Using the chatgpt_list_chatgpt_models_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> chatgpt_list_chatgpt_models_with_http_info(opts)

```ruby
begin
  # List ChatGPT models
  data, status_code, headers = api_instance.chatgpt_list_chatgpt_models_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_list_chatgpt_models_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country** | **String** | ISO-3166 alpha-2 egress country. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer

> Object chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer(prompt, brand, opts)

Measure a brand's visibility in a ChatGPT answer

Ask ChatGPT, then report whether the brand is mentioned, cited and how prominently.

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

api_instance = ScrapeBadger::ChatGPTApi.new
prompt = 'prompt_example' # String | The prompt to ask ChatGPT.
brand = 'brand_example' # String | Brand name to look for in the answer.
opts = {
  domain: 'domain_example', # String | Brand domain, for citation matching.
  aliases: 'aliases_example', # String | Comma-separated alternative names.
  competitors: 'competitors_example', # String | Comma-separated competitor names.
  country: 'country_example', # String | ISO-3166 alpha-2 egress country.
  web_search: 'web_search_example' # String | auto | force | off
}

begin
  # Measure a brand's visibility in a ChatGPT answer
  result = api_instance.chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer(prompt, brand, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer: #{e}"
end
```

#### Using the chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_with_http_info(prompt, brand, opts)

```ruby
begin
  # Measure a brand's visibility in a ChatGPT answer
  data, status_code, headers = api_instance.chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_with_http_info(prompt, brand, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The prompt to ask ChatGPT. |  |
| **brand** | **String** | Brand name to look for in the answer. |  |
| **domain** | **String** | Brand domain, for citation matching. | [optional] |
| **aliases** | **String** | Comma-separated alternative names. | [optional] |
| **competitors** | **String** | Comma-separated competitor names. | [optional] |
| **country** | **String** | ISO-3166 alpha-2 egress country. | [optional] |
| **web_search** | **String** | auto | force | off | [optional][default to &#39;force&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post

> Object chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post

Measure a brand's visibility in a ChatGPT answer (POST)

POST form, for longer prompts and larger competitor sets.

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

api_instance = ScrapeBadger::ChatGPTApi.new

begin
  # Measure a brand's visibility in a ChatGPT answer (POST)
  result = api_instance.chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post: #{e}"
end
```

#### Using the chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post_with_http_info

```ruby
begin
  # Measure a brand's visibility in a ChatGPT answer (POST)
  data, status_code, headers = api_instance.chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ChatGPTApi->chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post_with_http_info: #{e}"
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

