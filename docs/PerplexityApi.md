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
  country: 'country_example', # String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
  strict_country: true, # Boolean | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`.
  location: 'location_example', # String | Where the asker is: a city (tokyo, osaka, seoul, new-york, london, ...) or 'lat,lng' in decimal degrees. Perplexity answers a local-sounding question for it instead of the exit IP's city. It does not pick the egress: `country` does.
  html: true, # Boolean | Also return `answer_html`: the answer rendered as an HTML fragment, with each `[n]` citation linked to its source (`<a class=\"citation\" data-ref=\"n\">`). Raw HTML and unsafe links in the answer are dropped. Same price.
  raw: true, # Boolean | Also return `raw`: Perplexity's own final answer object as it sent it (answer blocks, web results, related queries, model and mode metadata), minus its thread write token. Every other field is parsed from it. Same price.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
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
| **strict_country** | **Boolean** | Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional][default to false] |
| **location** | **String** | Where the asker is: a city (tokyo, osaka, seoul, new-york, london, ...) or &#39;lat,lng&#39; in decimal degrees. Perplexity answers a local-sounding question for it instead of the exit IP&#39;s city. It does not pick the egress: &#x60;country&#x60; does. | [optional] |
| **html** | **Boolean** | Also return &#x60;answer_html&#x60;: the answer rendered as an HTML fragment, with each &#x60;[n]&#x60; citation linked to its source (&#x60;&lt;a class&#x3D;\&quot;citation\&quot; data-ref&#x3D;\&quot;n\&quot;&gt;&#x60;). Raw HTML and unsafe links in the answer are dropped. Same price. | [optional][default to false] |
| **raw** | **Boolean** | Also return &#x60;raw&#x60;: Perplexity&#39;s own final answer object as it sent it (answer blocks, web results, related queries, model and mode metadata), minus its thread write token. Every other field is parsed from it. Same price. | [optional][default to false] |
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


## perplexity_ask_perplexity_a_question_post

> Object perplexity_ask_perplexity_a_question_post(opts)

Ask Perplexity a question (POST)

POST form of `/ask`, for prompts too long for a query string. The JSON body takes the same fields as the query (`prompt`, `country`, `strict_country`, `location`, `html`, `raw`).

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
  # Ask Perplexity a question (POST)
  result = api_instance.perplexity_ask_perplexity_a_question_post(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_ask_perplexity_a_question_post: #{e}"
end
```

#### Using the perplexity_ask_perplexity_a_question_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> perplexity_ask_perplexity_a_question_post_with_http_info(opts)

```ruby
begin
  # Ask Perplexity a question (POST)
  data, status_code, headers = api_instance.perplexity_ask_perplexity_a_question_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_ask_perplexity_a_question_post_with_http_info: #{e}"
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
  country: 'country_example', # String | ISO-3166 alpha-2 egress country.
  strict_country: true, # Boolean | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`.
  location: 'location_example', # String | Where the asker is: a city (tokyo, osaka, seoul, new-york, london, ...) or 'lat,lng' in decimal degrees. Perplexity answers a local-sounding question for it instead of the exit IP's city. It does not pick the egress: `country` does.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
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
| **strict_country** | **Boolean** | Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional][default to false] |
| **location** | **String** | Where the asker is: a city (tokyo, osaka, seoul, new-york, london, ...) or &#39;lat,lng&#39; in decimal degrees. Perplexity answers a local-sounding question for it instead of the exit IP&#39;s city. It does not pick the egress: &#x60;country&#x60; does. | [optional] |
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


## perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post

> Object perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post(opts)

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
  # Measure a brand's visibility in a Perplexity answer (POST)
  result = api_instance.perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post: #{e}"
end
```

#### Using the perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post_with_http_info(opts)

```ruby
begin
  # Measure a brand's visibility in a Perplexity answer (POST)
  data, status_code, headers = api_instance.perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling PerplexityApi->perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post_with_http_info: #{e}"
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

