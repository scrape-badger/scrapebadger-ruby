# ScrapeBadger::RufusApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**rufus_amazon_rufus_scraper_health_check**](RufusApi.md#rufus_amazon_rufus_scraper_health_check) | **GET** /v1/rufus/health | Amazon Rufus scraper health check |
| [**rufus_amazon_rufus_scraper_health_check_head**](RufusApi.md#rufus_amazon_rufus_scraper_health_check_head) | **HEAD** /v1/rufus/health | Amazon Rufus scraper health check |
| [**rufus_ask_amazon_rufus_a_question**](RufusApi.md#rufus_ask_amazon_rufus_a_question) | **GET** /v1/rufus/ask | Ask Amazon Rufus a question |
| [**rufus_ask_amazon_rufus_a_question_post**](RufusApi.md#rufus_ask_amazon_rufus_a_question_post) | **POST** /v1/rufus/ask | Ask Amazon Rufus a question (POST) |
| [**rufus_list_amazon_rufus_models**](RufusApi.md#rufus_list_amazon_rufus_models) | **GET** /v1/rufus/models | List Amazon Rufus models |


## rufus_amazon_rufus_scraper_health_check

> Object rufus_amazon_rufus_scraper_health_check

Amazon Rufus scraper health check

Check health of the Amazon service that serves Rufus (accepts HEAD).

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

api_instance = ScrapeBadger::RufusApi.new

begin
  # Amazon Rufus scraper health check
  result = api_instance.rufus_amazon_rufus_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_amazon_rufus_scraper_health_check: #{e}"
end
```

#### Using the rufus_amazon_rufus_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> rufus_amazon_rufus_scraper_health_check_with_http_info

```ruby
begin
  # Amazon Rufus scraper health check
  data, status_code, headers = api_instance.rufus_amazon_rufus_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_amazon_rufus_scraper_health_check_with_http_info: #{e}"
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


## rufus_amazon_rufus_scraper_health_check_head

> Object rufus_amazon_rufus_scraper_health_check_head

Amazon Rufus scraper health check

Check health of the Amazon service that serves Rufus (accepts HEAD).

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

api_instance = ScrapeBadger::RufusApi.new

begin
  # Amazon Rufus scraper health check
  result = api_instance.rufus_amazon_rufus_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_amazon_rufus_scraper_health_check_head: #{e}"
end
```

#### Using the rufus_amazon_rufus_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> rufus_amazon_rufus_scraper_health_check_head_with_http_info

```ruby
begin
  # Amazon Rufus scraper health check
  data, status_code, headers = api_instance.rufus_amazon_rufus_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_amazon_rufus_scraper_health_check_head_with_http_info: #{e}"
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


## rufus_ask_amazon_rufus_a_question

> Object rufus_ask_amazon_rufus_a_question(prompt, opts)

Ask Amazon Rufus a question

Ask Alexa for Shopping (Rufus) and get its answer and product cards.

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

api_instance = ScrapeBadger::RufusApi.new
prompt = 'prompt_example' # String | The shopping question to ask (max 4000 characters).
opts = {
  asin: 'asin_example' # String | Optional product ASIN whose page should provide the shopping context.
}

begin
  # Ask Amazon Rufus a question
  result = api_instance.rufus_ask_amazon_rufus_a_question(prompt, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_ask_amazon_rufus_a_question: #{e}"
end
```

#### Using the rufus_ask_amazon_rufus_a_question_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> rufus_ask_amazon_rufus_a_question_with_http_info(prompt, opts)

```ruby
begin
  # Ask Amazon Rufus a question
  data, status_code, headers = api_instance.rufus_ask_amazon_rufus_a_question_with_http_info(prompt, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_ask_amazon_rufus_a_question_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The shopping question to ask (max 4000 characters). |  |
| **asin** | **String** | Optional product ASIN whose page should provide the shopping context. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## rufus_ask_amazon_rufus_a_question_post

> Object rufus_ask_amazon_rufus_a_question_post(rufus_ask_request)

Ask Amazon Rufus a question (POST)

POST form of `/ask`, accepting prompt and optional asin in the JSON body.

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

api_instance = ScrapeBadger::RufusApi.new
rufus_ask_request = ScrapeBadger::RufusAskRequest.new({prompt: 'prompt_example'}) # RufusAskRequest | 

begin
  # Ask Amazon Rufus a question (POST)
  result = api_instance.rufus_ask_amazon_rufus_a_question_post(rufus_ask_request)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_ask_amazon_rufus_a_question_post: #{e}"
end
```

#### Using the rufus_ask_amazon_rufus_a_question_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> rufus_ask_amazon_rufus_a_question_post_with_http_info(rufus_ask_request)

```ruby
begin
  # Ask Amazon Rufus a question (POST)
  data, status_code, headers = api_instance.rufus_ask_amazon_rufus_a_question_post_with_http_info(rufus_ask_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_ask_amazon_rufus_a_question_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rufus_ask_request** | [**RufusAskRequest**](RufusAskRequest.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## rufus_list_amazon_rufus_models

> Object rufus_list_amazon_rufus_models

List Amazon Rufus models

List the Amazon shopping assistant surface exposed by this API.

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

api_instance = ScrapeBadger::RufusApi.new

begin
  # List Amazon Rufus models
  result = api_instance.rufus_list_amazon_rufus_models
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_list_amazon_rufus_models: #{e}"
end
```

#### Using the rufus_list_amazon_rufus_models_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> rufus_list_amazon_rufus_models_with_http_info

```ruby
begin
  # List Amazon Rufus models
  data, status_code, headers = api_instance.rufus_list_amazon_rufus_models_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RufusApi->rufus_list_amazon_rufus_models_with_http_info: #{e}"
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

