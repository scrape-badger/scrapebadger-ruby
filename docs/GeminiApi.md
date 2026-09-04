# ScrapeBadger::GeminiApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**gemini_ask_gemini_a_question**](GeminiApi.md#gemini_ask_gemini_a_question) | **GET** /v1/gemini/ask | Ask Gemini a question |
| [**gemini_ask_gemini_a_question_post**](GeminiApi.md#gemini_ask_gemini_a_question_post) | **POST** /v1/gemini/ask | Ask Gemini a question (POST) |
| [**gemini_gemini_scraper_health_check**](GeminiApi.md#gemini_gemini_scraper_health_check) | **GET** /v1/gemini/health | Gemini scraper health check |
| [**gemini_gemini_scraper_health_check_head**](GeminiApi.md#gemini_gemini_scraper_health_check_head) | **HEAD** /v1/gemini/health | Gemini scraper health check |
| [**gemini_measure_a_brand_s_visibility_in_a_gemini_answer**](GeminiApi.md#gemini_measure_a_brand_s_visibility_in_a_gemini_answer) | **GET** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer |
| [**gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post**](GeminiApi.md#gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post) | **POST** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer (POST) |


## gemini_ask_gemini_a_question

> Object gemini_ask_gemini_a_question(prompt, opts)

Ask Gemini a question

Send a prompt to Gemini and get the answer plus the web sources it cited.

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

api_instance = ScrapeBadger::GeminiApi.new
prompt = 'prompt_example' # String | The prompt to send to Gemini (max 4096 characters).
opts = {
  country: 'country_example', # String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
  web_search: 'web_search_example', # String | auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened.
  image_url: 'image_url_example' # String | Public http(s) URL of an image to attach to the prompt. Gemini reads it and answers about it. POST also accepts `image_base64`. Exactly one of the two.
}

begin
  # Ask Gemini a question
  result = api_instance.gemini_ask_gemini_a_question(prompt, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_ask_gemini_a_question: #{e}"
end
```

#### Using the gemini_ask_gemini_a_question_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gemini_ask_gemini_a_question_with_http_info(prompt, opts)

```ruby
begin
  # Ask Gemini a question
  data, status_code, headers = api_instance.gemini_ask_gemini_a_question_with_http_info(prompt, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_ask_gemini_a_question_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The prompt to send to Gemini (max 4096 characters). |  |
| **country** | **String** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |
| **web_search** | **String** | auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional][default to &#39;auto&#39;] |
| **image_url** | **String** | Public http(s) URL of an image to attach to the prompt. Gemini reads it and answers about it. POST also accepts &#x60;image_base64&#x60;. Exactly one of the two. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gemini_ask_gemini_a_question_post

> Object gemini_ask_gemini_a_question_post

Ask Gemini a question (POST)

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

api_instance = ScrapeBadger::GeminiApi.new

begin
  # Ask Gemini a question (POST)
  result = api_instance.gemini_ask_gemini_a_question_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_ask_gemini_a_question_post: #{e}"
end
```

#### Using the gemini_ask_gemini_a_question_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gemini_ask_gemini_a_question_post_with_http_info

```ruby
begin
  # Ask Gemini a question (POST)
  data, status_code, headers = api_instance.gemini_ask_gemini_a_question_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_ask_gemini_a_question_post_with_http_info: #{e}"
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


## gemini_gemini_scraper_health_check

> Object gemini_gemini_scraper_health_check

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::GeminiApi.new

begin
  # Gemini scraper health check
  result = api_instance.gemini_gemini_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_gemini_scraper_health_check: #{e}"
end
```

#### Using the gemini_gemini_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gemini_gemini_scraper_health_check_with_http_info

```ruby
begin
  # Gemini scraper health check
  data, status_code, headers = api_instance.gemini_gemini_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_gemini_scraper_health_check_with_http_info: #{e}"
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


## gemini_gemini_scraper_health_check_head

> Object gemini_gemini_scraper_health_check_head

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::GeminiApi.new

begin
  # Gemini scraper health check
  result = api_instance.gemini_gemini_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_gemini_scraper_health_check_head: #{e}"
end
```

#### Using the gemini_gemini_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gemini_gemini_scraper_health_check_head_with_http_info

```ruby
begin
  # Gemini scraper health check
  data, status_code, headers = api_instance.gemini_gemini_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_gemini_scraper_health_check_head_with_http_info: #{e}"
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


## gemini_measure_a_brand_s_visibility_in_a_gemini_answer

> Object gemini_measure_a_brand_s_visibility_in_a_gemini_answer(prompt, brand, opts)

Measure a brand's visibility in a Gemini answer

Ask Gemini, then report whether the brand is mentioned, cited and how prominently.

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

api_instance = ScrapeBadger::GeminiApi.new
prompt = 'prompt_example' # String | The prompt to ask Gemini.
brand = 'brand_example' # String | Brand name to look for in the answer.
opts = {
  domain: 'domain_example', # String | Brand domain, for citation matching.
  aliases: 'aliases_example', # String | Comma-separated alternative names.
  competitors: 'competitors_example', # String | Comma-separated competitor names.
  country: 'country_example', # String | ISO-3166 alpha-2 egress country.
  web_search: 'web_search_example' # String | auto | force | off
}

begin
  # Measure a brand's visibility in a Gemini answer
  result = api_instance.gemini_measure_a_brand_s_visibility_in_a_gemini_answer(prompt, brand, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_measure_a_brand_s_visibility_in_a_gemini_answer: #{e}"
end
```

#### Using the gemini_measure_a_brand_s_visibility_in_a_gemini_answer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gemini_measure_a_brand_s_visibility_in_a_gemini_answer_with_http_info(prompt, brand, opts)

```ruby
begin
  # Measure a brand's visibility in a Gemini answer
  data, status_code, headers = api_instance.gemini_measure_a_brand_s_visibility_in_a_gemini_answer_with_http_info(prompt, brand, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_measure_a_brand_s_visibility_in_a_gemini_answer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The prompt to ask Gemini. |  |
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


## gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post

> Object gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post

Measure a brand's visibility in a Gemini answer (POST)

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

api_instance = ScrapeBadger::GeminiApi.new

begin
  # Measure a brand's visibility in a Gemini answer (POST)
  result = api_instance.gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post: #{e}"
end
```

#### Using the gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post_with_http_info

```ruby
begin
  # Measure a brand's visibility in a Gemini answer (POST)
  data, status_code, headers = api_instance.gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GeminiApi->gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post_with_http_info: #{e}"
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

