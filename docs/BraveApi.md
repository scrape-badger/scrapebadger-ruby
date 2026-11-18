# ScrapeBadger::BraveApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**brave_autocomplete**](BraveApi.md#brave_autocomplete) | **GET** /v1/brave/autocomplete | Autocomplete |
| [**brave_image_search**](BraveApi.md#brave_image_search) | **GET** /v1/brave/images | Image search |
| [**brave_list_supported_locales**](BraveApi.md#brave_list_supported_locales) | **GET** /v1/brave/locales | List supported locales |
| [**brave_news_search**](BraveApi.md#brave_news_search) | **GET** /v1/brave/news | News search |
| [**brave_video_search**](BraveApi.md#brave_video_search) | **GET** /v1/brave/videos | Video search |
| [**brave_web_search**](BraveApi.md#brave_web_search) | **GET** /v1/brave/search | Web search |


## brave_autocomplete

> <BraveAutocompleteResponse> brave_autocomplete(query, opts)

Autocomplete

Native search-box suggestions with entity descriptions and images. Two credits.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | 
opts = {
  country: 'us', # String | 
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Autocomplete
  result = api_instance.brave_autocomplete(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_autocomplete: #{e}"
end
```

#### Using the brave_autocomplete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveAutocompleteResponse>, Integer, Hash)> brave_autocomplete_with_http_info(query, opts)

```ruby
begin
  # Autocomplete
  data, status_code, headers = api_instance.brave_autocomplete_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveAutocompleteResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_autocomplete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **country** | **String** |  | [optional][default to &#39;us&#39;] |
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

### Return type

[**BraveAutocompleteResponse**](BraveAutocompleteResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_image_search

> <BraveResponse> brave_image_search(query, opts)

Image search

Native image batch with original URLs, source pages, thumbnails and dimensions.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | Native Brave search query
opts = {
  country: 'us', # String | Native result region; see /locales
  ui_language: 'en-us', # String | UI labels/date language; does not restrict result language
  safe_search: 'off', # String | 
  count: 56, # Integer | Slice the initial native image batch
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Image search
  result = api_instance.brave_image_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_image_search: #{e}"
end
```

#### Using the brave_image_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveResponse>, Integer, Hash)> brave_image_search_with_http_info(query, opts)

```ruby
begin
  # Image search
  data, status_code, headers = api_instance.brave_image_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_image_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Native Brave search query |  |
| **country** | **String** | Native result region; see /locales | [optional][default to &#39;us&#39;] |
| **ui_language** | **String** | UI labels/date language; does not restrict result language | [optional][default to &#39;en-us&#39;] |
| **safe_search** | **String** |  | [optional][default to &#39;moderate&#39;] |
| **count** | **Integer** | Slice the initial native image batch | [optional][default to 50] |
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

### Return type

[**BraveResponse**](BraveResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_list_supported_locales

> <BraveLocalesResponse> brave_list_supported_locales(opts)

List supported locales

Native country and UI-language choices. Free; result language is a separate preference.

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

api_instance = ScrapeBadger::BraveApi.new
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
  # List supported locales
  result = api_instance.brave_list_supported_locales(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_list_supported_locales: #{e}"
end
```

#### Using the brave_list_supported_locales_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveLocalesResponse>, Integer, Hash)> brave_list_supported_locales_with_http_info(opts)

```ruby
begin
  # List supported locales
  data, status_code, headers = api_instance.brave_list_supported_locales_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveLocalesResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_list_supported_locales_with_http_info: #{e}"
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

[**BraveLocalesResponse**](BraveLocalesResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_news_search

> <BraveResponse> brave_news_search(query, opts)

News search

Native news batch; relative source dates stay display strings.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | Native Brave search query
opts = {
  country: 'us', # String | Native result region; see /locales
  ui_language: 'en-us', # String | UI labels/date language; does not restrict result language
  safe_search: 'off', # String | 
  count: 56, # Integer | Slice the initial native news batch
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # News search
  result = api_instance.brave_news_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_news_search: #{e}"
end
```

#### Using the brave_news_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveResponse>, Integer, Hash)> brave_news_search_with_http_info(query, opts)

```ruby
begin
  # News search
  data, status_code, headers = api_instance.brave_news_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_news_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Native Brave search query |  |
| **country** | **String** | Native result region; see /locales | [optional][default to &#39;us&#39;] |
| **ui_language** | **String** | UI labels/date language; does not restrict result language | [optional][default to &#39;en-us&#39;] |
| **safe_search** | **String** |  | [optional][default to &#39;moderate&#39;] |
| **count** | **Integer** | Slice the initial native news batch | [optional][default to 35] |
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

### Return type

[**BraveResponse**](BraveResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_video_search

> <BravePagedResponse> brave_video_search(query, opts)

Video search

Native video results with duration, creator, publisher and verified page ordinals.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | Native Brave search query
opts = {
  country: 'us', # String | Native result region; see /locales
  ui_language: 'en-us', # String | UI labels/date language; does not restrict result language
  safe_search: 'off', # String | 
  page: 56, # Integer | 1-based native page ordinal
  count: 56, # Integer | 
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Video search
  result = api_instance.brave_video_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_video_search: #{e}"
end
```

#### Using the brave_video_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BravePagedResponse>, Integer, Hash)> brave_video_search_with_http_info(query, opts)

```ruby
begin
  # Video search
  data, status_code, headers = api_instance.brave_video_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BravePagedResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_video_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Native Brave search query |  |
| **country** | **String** | Native result region; see /locales | [optional][default to &#39;us&#39;] |
| **ui_language** | **String** | UI labels/date language; does not restrict result language | [optional][default to &#39;en-us&#39;] |
| **safe_search** | **String** |  | [optional][default to &#39;moderate&#39;] |
| **page** | **Integer** | 1-based native page ordinal | [optional][default to 1] |
| **count** | **Integer** |  | [optional][default to 50] |
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

### Return type

[**BravePagedResponse**](BravePagedResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brave_web_search

> <BraveSearchResponse> brave_web_search(query, opts)

Web search

Native Brave organic results, rich source blocks and page metadata. Seven credits.

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

api_instance = ScrapeBadger::BraveApi.new
query = 'query_example' # String | Native Brave search query
opts = {
  country: 'us', # String | Native result region; see /locales
  ui_language: 'en-us', # String | UI labels/date language; does not restrict result language
  safe_search: 'off', # String | 
  page: 56, # Integer | 1-based native page ordinal
  count: 56, # Integer | Slice one native page; does not change native page boundaries
  freshness: 'any', # String | 
  spellcheck: true, # Boolean | Allow native spelling correction
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Web search
  result = api_instance.brave_web_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_web_search: #{e}"
end
```

#### Using the brave_web_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BraveSearchResponse>, Integer, Hash)> brave_web_search_with_http_info(query, opts)

```ruby
begin
  # Web search
  data, status_code, headers = api_instance.brave_web_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BraveSearchResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BraveApi->brave_web_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Native Brave search query |  |
| **country** | **String** | Native result region; see /locales | [optional][default to &#39;us&#39;] |
| **ui_language** | **String** | UI labels/date language; does not restrict result language | [optional][default to &#39;en-us&#39;] |
| **safe_search** | **String** |  | [optional][default to &#39;moderate&#39;] |
| **page** | **Integer** | 1-based native page ordinal | [optional][default to 1] |
| **count** | **Integer** | Slice one native page; does not change native page boundaries | [optional][default to 20] |
| **freshness** | **String** |  | [optional][default to &#39;any&#39;] |
| **spellcheck** | **Boolean** | Allow native spelling correction | [optional][default to false] |
| **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] |
| **x_callback_url** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] |
| **idempotency_key** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] |
| **async** | **Boolean** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] |
| **async_wait** | **Integer** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] |
| **callback_url** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] |
| **idempotency_key2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] |

### Return type

[**BraveSearchResponse**](BraveSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

