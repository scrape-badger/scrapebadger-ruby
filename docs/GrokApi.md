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
  web_search: 'web_search_example', # String | Web and X search: auto, force, or off.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
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
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## grok_ask_grok_a_question_post

> Object grok_ask_grok_a_question_post(opts)

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
opts = {
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Ask Grok a question (POST)
  result = api_instance.grok_ask_grok_a_question_post(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_ask_grok_a_question_post: #{e}"
end
```

#### Using the grok_ask_grok_a_question_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_ask_grok_a_question_post_with_http_info(opts)

```ruby
begin
  # Ask Grok a question (POST)
  data, status_code, headers = api_instance.grok_ask_grok_a_question_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_ask_grok_a_question_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## grok_get_a_grok_conversation

> Object grok_get_a_grok_conversation(conversation_id, opts)

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
opts = {
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get a Grok conversation
  result = api_instance.grok_get_a_grok_conversation(conversation_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_get_a_grok_conversation: #{e}"
end
```

#### Using the grok_get_a_grok_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_get_a_grok_conversation_with_http_info(conversation_id, opts)

```ruby
begin
  # Get a Grok conversation
  data, status_code, headers = api_instance.grok_get_a_grok_conversation_with_http_info(conversation_id, opts)
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
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

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

> Object grok_list_grok_assistant_modes(opts)

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
opts = {
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # List Grok assistant modes
  result = api_instance.grok_list_grok_assistant_modes(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_list_grok_assistant_modes: #{e}"
end
```

#### Using the grok_list_grok_assistant_modes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_list_grok_assistant_modes_with_http_info(opts)

```ruby
begin
  # List Grok assistant modes
  data, status_code, headers = api_instance.grok_list_grok_assistant_modes_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_list_grok_assistant_modes_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

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
  web_search: 'web_search_example', # String | Web and X search mode.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
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
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## grok_measure_brand_visibility_in_grok_post

> Object grok_measure_brand_visibility_in_grok_post(opts)

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
opts = {
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Measure brand visibility in Grok (POST)
  result = api_instance.grok_measure_brand_visibility_in_grok_post(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_measure_brand_visibility_in_grok_post: #{e}"
end
```

#### Using the grok_measure_brand_visibility_in_grok_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> grok_measure_brand_visibility_in_grok_post_with_http_info(opts)

```ruby
begin
  # Measure brand visibility in Grok (POST)
  data, status_code, headers = api_instance.grok_measure_brand_visibility_in_grok_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GrokApi->grok_measure_brand_visibility_in_grok_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

