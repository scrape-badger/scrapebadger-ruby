# ScrapeBadger::MetaAiApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**meta_ai_ask_meta_ai_a_question**](MetaAiApi.md#meta_ai_ask_meta_ai_a_question) | **GET** /v1/meta-ai/ask | Ask Meta AI a question |
| [**meta_ai_ask_meta_ai_a_question_post**](MetaAiApi.md#meta_ai_ask_meta_ai_a_question_post) | **POST** /v1/meta-ai/ask | Ask Meta AI a question (POST) |
| [**meta_ai_list_meta_ai_assistant_modes**](MetaAiApi.md#meta_ai_list_meta_ai_assistant_modes) | **GET** /v1/meta-ai/models | List Meta AI assistant modes |
| [**meta_ai_meta_ai_scraper_health_check**](MetaAiApi.md#meta_ai_meta_ai_scraper_health_check) | **GET** /v1/meta-ai/health | Meta AI scraper health check |
| [**meta_ai_meta_ai_scraper_health_check_head**](MetaAiApi.md#meta_ai_meta_ai_scraper_health_check_head) | **HEAD** /v1/meta-ai/health | Meta AI scraper health check |


## meta_ai_ask_meta_ai_a_question

> Object meta_ai_ask_meta_ai_a_question(prompt, opts)

Ask Meta AI a question

Send a prompt to meta.ai and get the answer (anonymous, no Meta account).

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

api_instance = ScrapeBadger::MetaAiApi.new
prompt = 'prompt_example' # String | The prompt to send to Meta AI (max 4000 characters).
opts = {
  country: 'country_example' # String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
}

begin
  # Ask Meta AI a question
  result = api_instance.meta_ai_ask_meta_ai_a_question(prompt, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_ask_meta_ai_a_question: #{e}"
end
```

#### Using the meta_ai_ask_meta_ai_a_question_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> meta_ai_ask_meta_ai_a_question_with_http_info(prompt, opts)

```ruby
begin
  # Ask Meta AI a question
  data, status_code, headers = api_instance.meta_ai_ask_meta_ai_a_question_with_http_info(prompt, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_ask_meta_ai_a_question_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The prompt to send to Meta AI (max 4000 characters). |  |
| **country** | **String** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## meta_ai_ask_meta_ai_a_question_post

> Object meta_ai_ask_meta_ai_a_question_post

Ask Meta AI a question (POST)

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

api_instance = ScrapeBadger::MetaAiApi.new

begin
  # Ask Meta AI a question (POST)
  result = api_instance.meta_ai_ask_meta_ai_a_question_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_ask_meta_ai_a_question_post: #{e}"
end
```

#### Using the meta_ai_ask_meta_ai_a_question_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> meta_ai_ask_meta_ai_a_question_post_with_http_info

```ruby
begin
  # Ask Meta AI a question (POST)
  data, status_code, headers = api_instance.meta_ai_ask_meta_ai_a_question_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_ask_meta_ai_a_question_post_with_http_info: #{e}"
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


## meta_ai_list_meta_ai_assistant_modes

> Object meta_ai_list_meta_ai_assistant_modes(opts)

List Meta AI assistant modes

Assistant modes meta.ai currently serves to an anonymous visitor.

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

api_instance = ScrapeBadger::MetaAiApi.new
opts = {
  country: 'country_example' # String | ISO-3166 alpha-2 egress country.
}

begin
  # List Meta AI assistant modes
  result = api_instance.meta_ai_list_meta_ai_assistant_modes(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_list_meta_ai_assistant_modes: #{e}"
end
```

#### Using the meta_ai_list_meta_ai_assistant_modes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> meta_ai_list_meta_ai_assistant_modes_with_http_info(opts)

```ruby
begin
  # List Meta AI assistant modes
  data, status_code, headers = api_instance.meta_ai_list_meta_ai_assistant_modes_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_list_meta_ai_assistant_modes_with_http_info: #{e}"
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


## meta_ai_meta_ai_scraper_health_check

> Object meta_ai_meta_ai_scraper_health_check

Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::MetaAiApi.new

begin
  # Meta AI scraper health check
  result = api_instance.meta_ai_meta_ai_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_meta_ai_scraper_health_check: #{e}"
end
```

#### Using the meta_ai_meta_ai_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> meta_ai_meta_ai_scraper_health_check_with_http_info

```ruby
begin
  # Meta AI scraper health check
  data, status_code, headers = api_instance.meta_ai_meta_ai_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_meta_ai_scraper_health_check_with_http_info: #{e}"
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


## meta_ai_meta_ai_scraper_health_check_head

> Object meta_ai_meta_ai_scraper_health_check_head

Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::MetaAiApi.new

begin
  # Meta AI scraper health check
  result = api_instance.meta_ai_meta_ai_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_meta_ai_scraper_health_check_head: #{e}"
end
```

#### Using the meta_ai_meta_ai_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> meta_ai_meta_ai_scraper_health_check_head_with_http_info

```ruby
begin
  # Meta AI scraper health check
  data, status_code, headers = api_instance.meta_ai_meta_ai_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling MetaAiApi->meta_ai_meta_ai_scraper_health_check_head_with_http_info: #{e}"
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

