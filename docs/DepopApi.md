# ScrapeBadger::DepopApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**depop_depop_scraper_health_check**](DepopApi.md#depop_depop_scraper_health_check) | **GET** /v1/depop/health | Depop scraper health check |
| [**depop_depop_scraper_health_check_head**](DepopApi.md#depop_depop_scraper_health_check_head) | **HEAD** /v1/depop/health | Depop scraper health check |
| [**depop_get_a_user_s_products**](DepopApi.md#depop_get_a_user_s_products) | **GET** /v1/depop/users/{username}/products | Get a user&#39;s products |
| [**depop_get_product_detail**](DepopApi.md#depop_get_product_detail) | **GET** /v1/depop/products/{product_id} | Get product detail |
| [**depop_get_shop_user_profile**](DepopApi.md#depop_get_shop_user_profile) | **GET** /v1/depop/users/{username} | Get shop/user profile |
| [**depop_list_markets**](DepopApi.md#depop_list_markets) | **GET** /v1/depop/markets | List markets |
| [**depop_search_depop_products**](DepopApi.md#depop_search_depop_products) | **GET** /v1/depop/search | Search Depop products |


## depop_depop_scraper_health_check

> Object depop_depop_scraper_health_check

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::DepopApi.new

begin
  # Depop scraper health check
  result = api_instance.depop_depop_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_depop_scraper_health_check: #{e}"
end
```

#### Using the depop_depop_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_depop_scraper_health_check_with_http_info

```ruby
begin
  # Depop scraper health check
  data, status_code, headers = api_instance.depop_depop_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_depop_scraper_health_check_with_http_info: #{e}"
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


## depop_depop_scraper_health_check_head

> Object depop_depop_scraper_health_check_head

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::DepopApi.new

begin
  # Depop scraper health check
  result = api_instance.depop_depop_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_depop_scraper_health_check_head: #{e}"
end
```

#### Using the depop_depop_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_depop_scraper_health_check_head_with_http_info

```ruby
begin
  # Depop scraper health check
  data, status_code, headers = api_instance.depop_depop_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_depop_scraper_health_check_head_with_http_info: #{e}"
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


## depop_get_a_user_s_products

> Object depop_get_a_user_s_products(username, opts)

Get a user's products

A user's active listings (cursor-paginated).

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

api_instance = ScrapeBadger::DepopApi.new
username = 'username_example' # String | 
opts = {
  market: 'market_example', # String | Market code
  per_page: 56, # Integer | 
  cursor: 'cursor_example', # String | Pagination cursor
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get a user's products
  result = api_instance.depop_get_a_user_s_products(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_a_user_s_products: #{e}"
end
```

#### Using the depop_get_a_user_s_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_get_a_user_s_products_with_http_info(username, opts)

```ruby
begin
  # Get a user's products
  data, status_code, headers = api_instance.depop_get_a_user_s_products_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_a_user_s_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **market** | **String** | Market code | [optional][default to &#39;us&#39;] |
| **per_page** | **Integer** |  | [optional][default to 24] |
| **cursor** | **String** | Pagination cursor | [optional] |
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


## depop_get_product_detail

> Object depop_get_product_detail(product_id, opts)

Get product detail

Full detail for a single product (by numeric id or slug).

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

api_instance = ScrapeBadger::DepopApi.new
product_id = 'product_id_example' # String | 
opts = {
  market: 'market_example', # String | Market code
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get product detail
  result = api_instance.depop_get_product_detail(product_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_product_detail: #{e}"
end
```

#### Using the depop_get_product_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_get_product_detail_with_http_info(product_id, opts)

```ruby
begin
  # Get product detail
  data, status_code, headers = api_instance.depop_get_product_detail_with_http_info(product_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_product_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |
| **market** | **String** | Market code | [optional][default to &#39;us&#39;] |
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


## depop_get_shop_user_profile

> Object depop_get_shop_user_profile(username, opts)

Get shop/user profile

Public shop/user profile by username.

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

api_instance = ScrapeBadger::DepopApi.new
username = 'username_example' # String | 
opts = {
  market: 'market_example', # String | Market code
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get shop/user profile
  result = api_instance.depop_get_shop_user_profile(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_shop_user_profile: #{e}"
end
```

#### Using the depop_get_shop_user_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_get_shop_user_profile_with_http_info(username, opts)

```ruby
begin
  # Get shop/user profile
  data, status_code, headers = api_instance.depop_get_shop_user_profile_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_get_shop_user_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **market** | **String** | Market code | [optional][default to &#39;us&#39;] |
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


## depop_list_markets

> Object depop_list_markets(opts)

List markets

List supported Depop markets (country + currency).

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

api_instance = ScrapeBadger::DepopApi.new
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
  # List markets
  result = api_instance.depop_list_markets(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_list_markets: #{e}"
end
```

#### Using the depop_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_list_markets_with_http_info(opts)

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.depop_list_markets_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_list_markets_with_http_info: #{e}"
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


## depop_search_depop_products

> Object depop_search_depop_products(query, opts)

Search Depop products

Search the Depop catalog with filters (cursor-paginated).

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

api_instance = ScrapeBadger::DepopApi.new
query = 'query_example' # String | Search text, e.g. 'nike vintage'
opts = {
  market: 'market_example', # String | Market code (us, gb, au, it, fr, ...)
  per_page: 56, # Integer | Results per page
  cursor: 'cursor_example', # String | Pagination cursor (from previous page)
  price_min: 8.14, # Float | Minimum price
  price_max: 8.14, # Float | Maximum price
  brands: 'brands_example', # String | Comma-separated brand IDs
  categories: 'categories_example', # String | Comma-separated category IDs
  sizes: 'sizes_example', # String | Comma-separated size IDs
  conditions: 'conditions_example', # String | Comma-separated condition slugs (brand_new, used_excellent, ...)
  gender: 'gender_example', # String | male | female
  sort: 'sort_example', # String | relevance (default) | priceAscending | priceDescending
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Search Depop products
  result = api_instance.depop_search_depop_products(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_search_depop_products: #{e}"
end
```

#### Using the depop_search_depop_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> depop_search_depop_products_with_http_info(query, opts)

```ruby
begin
  # Search Depop products
  data, status_code, headers = api_instance.depop_search_depop_products_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling DepopApi->depop_search_depop_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search text, e.g. &#39;nike vintage&#39; |  |
| **market** | **String** | Market code (us, gb, au, it, fr, ...) | [optional][default to &#39;us&#39;] |
| **per_page** | **Integer** | Results per page | [optional][default to 24] |
| **cursor** | **String** | Pagination cursor (from previous page) | [optional] |
| **price_min** | **Float** | Minimum price | [optional] |
| **price_max** | **Float** | Maximum price | [optional] |
| **brands** | **String** | Comma-separated brand IDs | [optional] |
| **categories** | **String** | Comma-separated category IDs | [optional] |
| **sizes** | **String** | Comma-separated size IDs | [optional] |
| **conditions** | **String** | Comma-separated condition slugs (brand_new, used_excellent, ...) | [optional] |
| **gender** | **String** | male | female | [optional] |
| **sort** | **String** | relevance (default) | priceAscending | priceDescending | [optional] |
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

