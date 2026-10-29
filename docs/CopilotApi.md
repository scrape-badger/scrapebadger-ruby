# ScrapeBadger::CopilotApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**copilot_ask_copilot_a_question**](CopilotApi.md#copilot_ask_copilot_a_question) | **GET** /v1/copilot/ask | Ask Copilot a question |
| [**copilot_ask_copilot_a_question_post**](CopilotApi.md#copilot_ask_copilot_a_question_post) | **POST** /v1/copilot/ask | Ask Copilot a question (POST) |
| [**copilot_copilot_scraper_health_check**](CopilotApi.md#copilot_copilot_scraper_health_check) | **GET** /v1/copilot/health | Copilot scraper health check |
| [**copilot_copilot_scraper_health_check_head**](CopilotApi.md#copilot_copilot_scraper_health_check_head) | **HEAD** /v1/copilot/health | Copilot scraper health check |
| [**copilot_list_copilot_markets**](CopilotApi.md#copilot_list_copilot_markets) | **GET** /v1/copilot/markets | List Copilot markets |
| [**copilot_measure_a_brand_s_visibility_in_a_copilot_answer**](CopilotApi.md#copilot_measure_a_brand_s_visibility_in_a_copilot_answer) | **GET** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer |
| [**copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post**](CopilotApi.md#copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post) | **POST** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer (POST) |


## copilot_ask_copilot_a_question

> Object copilot_ask_copilot_a_question(prompt, opts)

Ask Copilot a question

Ask Microsoft Copilot (Copilot Search in Bing) and get the answer plus its cited sources.

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

api_instance = ScrapeBadger::CopilotApi.new
prompt = 'prompt_example' # String | The prompt to send to Copilot (max 2000 characters).
opts = {
  country: 'country_example', # String | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market.
  market: 'market_example', # String | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's.
  strict_country: true # Boolean | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`.
}

begin
  # Ask Copilot a question
  result = api_instance.copilot_ask_copilot_a_question(prompt, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_ask_copilot_a_question: #{e}"
end
```

#### Using the copilot_ask_copilot_a_question_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> copilot_ask_copilot_a_question_with_http_info(prompt, opts)

```ruby
begin
  # Ask Copilot a question
  data, status_code, headers = api_instance.copilot_ask_copilot_a_question_with_http_info(prompt, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_ask_copilot_a_question_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The prompt to send to Copilot (max 2000 characters). |  |
| **country** | **String** | ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional] |
| **market** | **String** | Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional] |
| **strict_country** | **Boolean** | Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional][default to false] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## copilot_ask_copilot_a_question_post

> Object copilot_ask_copilot_a_question_post

Ask Copilot a question (POST)

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

api_instance = ScrapeBadger::CopilotApi.new

begin
  # Ask Copilot a question (POST)
  result = api_instance.copilot_ask_copilot_a_question_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_ask_copilot_a_question_post: #{e}"
end
```

#### Using the copilot_ask_copilot_a_question_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> copilot_ask_copilot_a_question_post_with_http_info

```ruby
begin
  # Ask Copilot a question (POST)
  data, status_code, headers = api_instance.copilot_ask_copilot_a_question_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_ask_copilot_a_question_post_with_http_info: #{e}"
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


## copilot_copilot_scraper_health_check

> Object copilot_copilot_scraper_health_check

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::CopilotApi.new

begin
  # Copilot scraper health check
  result = api_instance.copilot_copilot_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_copilot_scraper_health_check: #{e}"
end
```

#### Using the copilot_copilot_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> copilot_copilot_scraper_health_check_with_http_info

```ruby
begin
  # Copilot scraper health check
  data, status_code, headers = api_instance.copilot_copilot_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_copilot_scraper_health_check_with_http_info: #{e}"
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


## copilot_copilot_scraper_health_check_head

> Object copilot_copilot_scraper_health_check_head

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::CopilotApi.new

begin
  # Copilot scraper health check
  result = api_instance.copilot_copilot_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_copilot_scraper_health_check_head: #{e}"
end
```

#### Using the copilot_copilot_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> copilot_copilot_scraper_health_check_head_with_http_info

```ruby
begin
  # Copilot scraper health check
  data, status_code, headers = api_instance.copilot_copilot_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_copilot_scraper_health_check_head_with_http_info: #{e}"
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


## copilot_list_copilot_markets

> Object copilot_list_copilot_markets

List Copilot markets

The Bing markets Copilot can be asked in.

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

api_instance = ScrapeBadger::CopilotApi.new

begin
  # List Copilot markets
  result = api_instance.copilot_list_copilot_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_list_copilot_markets: #{e}"
end
```

#### Using the copilot_list_copilot_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> copilot_list_copilot_markets_with_http_info

```ruby
begin
  # List Copilot markets
  data, status_code, headers = api_instance.copilot_list_copilot_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_list_copilot_markets_with_http_info: #{e}"
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


## copilot_measure_a_brand_s_visibility_in_a_copilot_answer

> Object copilot_measure_a_brand_s_visibility_in_a_copilot_answer(prompt, brand, opts)

Measure a brand's visibility in a Copilot answer

Ask Copilot, then report whether the brand is mentioned, cited and how prominently.

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

api_instance = ScrapeBadger::CopilotApi.new
prompt = 'prompt_example' # String | The prompt to ask Copilot.
brand = 'brand_example' # String | Brand name to look for in the answer.
opts = {
  domain: 'domain_example', # String | Brand domain, for citation matching.
  aliases: 'aliases_example', # String | Comma-separated alternative names.
  competitors: 'competitors_example', # String | Comma-separated competitor names.
  country: 'country_example', # String | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market.
  market: 'market_example', # String | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's.
  strict_country: true # Boolean | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`.
}

begin
  # Measure a brand's visibility in a Copilot answer
  result = api_instance.copilot_measure_a_brand_s_visibility_in_a_copilot_answer(prompt, brand, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_measure_a_brand_s_visibility_in_a_copilot_answer: #{e}"
end
```

#### Using the copilot_measure_a_brand_s_visibility_in_a_copilot_answer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> copilot_measure_a_brand_s_visibility_in_a_copilot_answer_with_http_info(prompt, brand, opts)

```ruby
begin
  # Measure a brand's visibility in a Copilot answer
  data, status_code, headers = api_instance.copilot_measure_a_brand_s_visibility_in_a_copilot_answer_with_http_info(prompt, brand, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_measure_a_brand_s_visibility_in_a_copilot_answer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prompt** | **String** | The prompt to ask Copilot. |  |
| **brand** | **String** | Brand name to look for in the answer. |  |
| **domain** | **String** | Brand domain, for citation matching. | [optional] |
| **aliases** | **String** | Comma-separated alternative names. | [optional] |
| **competitors** | **String** | Comma-separated competitor names. | [optional] |
| **country** | **String** | ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional] |
| **market** | **String** | Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional] |
| **strict_country** | **Boolean** | Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional][default to false] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post

> Object copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post

Measure a brand's visibility in a Copilot answer (POST)

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

api_instance = ScrapeBadger::CopilotApi.new

begin
  # Measure a brand's visibility in a Copilot answer (POST)
  result = api_instance.copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post: #{e}"
end
```

#### Using the copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post_with_http_info

```ruby
begin
  # Measure a brand's visibility in a Copilot answer (POST)
  data, status_code, headers = api_instance.copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling CopilotApi->copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post_with_http_info: #{e}"
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

