# ScrapeBadger::PerplexityApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**perplexity_ask_perplexity_a_question**](PerplexityApi.md#perplexity_ask_perplexity_a_question) | **GET** /v1/perplexity/ask | Ask Perplexity a question |
| [**perplexity_ask_perplexity_a_question_post**](PerplexityApi.md#perplexity_ask_perplexity_a_question_post) | **POST** /v1/perplexity/ask | Ask Perplexity a question (POST) |
| [**perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer**](PerplexityApi.md#perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer) | **GET** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer |
| [**perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post**](PerplexityApi.md#perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post) | **POST** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer (POST) |
| [**perplexity_perplexity_scraper_health_check**](PerplexityApi.md#perplexity_perplexity_scraper_health_check) | **GET** /v1/perplexity/health | Perplexity scraper health check |
| [**perplexity_perplexity_scraper_health_check_head**](PerplexityApi.md#perplexity_perplexity_scraper_health_check_head) | **HEAD** /v1/perplexity/health | Perplexity scraper health check |


## perplexity_ask_perplexity_a_question

> Object perplexity_ask_perplexity_a_question(prompt, opts)

Ask Perplexity a question

Send a prompt to Perplexity and get the answer plus the web sources it cited.

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

api_instance = ScrapeBadger::PerplexityApi.new
prompt = 'prompt_example' # String | The prompt to send to Perplexity (max 4096 characters).
opts = {
  country: 'country_example' # String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
}

begin
  # Ask Perplexity a question
  result = api_instance.perplexity_ask_perplexity_a_question(prompt, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_ask_perplexity_a_question: #{e}"
end
```

#### Using the perplexity_ask_perplexity_a_question_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> perplexity_ask_perplexity_a_question_with_http_info(prompt, opts)

```ruby
begin
  # Ask Perplexity a question
  data, status_code, headers = api_instance.perplexity_ask_perplexity_a_question_with_http_info(prompt, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_ask_perplexity_a_question_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The prompt to send to Perplexity (max 4096 characters). |  |
| **country** | **String** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## perplexity_ask_perplexity_a_question_post

> Object perplexity_ask_perplexity_a_question_post

Ask Perplexity a question (POST)

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

api_instance = ScrapeBadger::PerplexityApi.new

begin
  # Ask Perplexity a question (POST)
  result = api_instance.perplexity_ask_perplexity_a_question_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_ask_perplexity_a_question_post: #{e}"
end
```

#### Using the perplexity_ask_perplexity_a_question_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> perplexity_ask_perplexity_a_question_post_with_http_info

```ruby
begin
  # Ask Perplexity a question (POST)
  data, status_code, headers = api_instance.perplexity_ask_perplexity_a_question_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_ask_perplexity_a_question_post_with_http_info: #{e}"
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


## perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer

> Object perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer(prompt, brand, opts)

Measure a brand's visibility in a Perplexity answer

Ask Perplexity, then report whether the brand is mentioned, cited and how prominently.

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

api_instance = ScrapeBadger::PerplexityApi.new
prompt = 'prompt_example' # String | The prompt to ask Perplexity.
brand = 'brand_example' # String | Brand name to look for in the answer.
opts = {
  domain: 'domain_example', # String | Brand domain, for citation matching.
  aliases: 'aliases_example', # String | Comma-separated alternative names.
  competitors: 'competitors_example', # String | Comma-separated competitor names.
  country: 'country_example' # String | ISO-3166 alpha-2 egress country.
}

begin
  # Measure a brand's visibility in a Perplexity answer
  result = api_instance.perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer(prompt, brand, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer: #{e}"
end
```

#### Using the perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_with_http_info(prompt, brand, opts)

```ruby
begin
  # Measure a brand's visibility in a Perplexity answer
  data, status_code, headers = api_instance.perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_with_http_info(prompt, brand, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The prompt to ask Perplexity. |  |
| **brand** | **String** | Brand name to look for in the answer. |  |
| **domain** | **String** | Brand domain, for citation matching. | [optional] |
| **aliases** | **String** | Comma-separated alternative names. | [optional] |
| **competitors** | **String** | Comma-separated competitor names. | [optional] |
| **country** | **String** | ISO-3166 alpha-2 egress country. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post

> Object perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post

Measure a brand's visibility in a Perplexity answer (POST)

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

api_instance = ScrapeBadger::PerplexityApi.new

begin
  # Measure a brand's visibility in a Perplexity answer (POST)
  result = api_instance.perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post: #{e}"
end
```

#### Using the perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post_with_http_info

```ruby
begin
  # Measure a brand's visibility in a Perplexity answer (POST)
  data, status_code, headers = api_instance.perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post_with_http_info: #{e}"
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


## perplexity_perplexity_scraper_health_check

> Object perplexity_perplexity_scraper_health_check

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::PerplexityApi.new

begin
  # Perplexity scraper health check
  result = api_instance.perplexity_perplexity_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_perplexity_scraper_health_check: #{e}"
end
```

#### Using the perplexity_perplexity_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> perplexity_perplexity_scraper_health_check_with_http_info

```ruby
begin
  # Perplexity scraper health check
  data, status_code, headers = api_instance.perplexity_perplexity_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_perplexity_scraper_health_check_with_http_info: #{e}"
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


## perplexity_perplexity_scraper_health_check_head

> Object perplexity_perplexity_scraper_health_check_head

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::PerplexityApi.new

begin
  # Perplexity scraper health check
  result = api_instance.perplexity_perplexity_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_perplexity_scraper_health_check_head: #{e}"
end
```

#### Using the perplexity_perplexity_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> perplexity_perplexity_scraper_health_check_head_with_http_info

```ruby
begin
  # Perplexity scraper health check
  data, status_code, headers = api_instance.perplexity_perplexity_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_perplexity_scraper_health_check_head_with_http_info: #{e}"
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

