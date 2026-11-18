# ScrapeBadger::GumtreeApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**gumtree_get_listing**](GumtreeApi.md#gumtree_get_listing) | **GET** /v1/gumtree/listings/{listing_id} | Get listing |
| [**gumtree_get_search_filters**](GumtreeApi.md#gumtree_get_search_filters) | **GET** /v1/gumtree/search/filters | Get search filters |
| [**gumtree_get_seller_listings**](GumtreeApi.md#gumtree_get_seller_listings) | **GET** /v1/gumtree/listings/{listing_id}/seller-listings | Get seller listings |
| [**gumtree_gumtree_scraper_health_check**](GumtreeApi.md#gumtree_gumtree_scraper_health_check) | **GET** /v1/gumtree/health | Gumtree scraper health check |
| [**gumtree_gumtree_scraper_health_check_head**](GumtreeApi.md#gumtree_gumtree_scraper_health_check_head) | **HEAD** /v1/gumtree/health | Gumtree scraper health check |
| [**gumtree_list_categories**](GumtreeApi.md#gumtree_list_categories) | **GET** /v1/gumtree/categories | List categories |
| [**gumtree_list_locations**](GumtreeApi.md#gumtree_list_locations) | **GET** /v1/gumtree/locations | List locations |
| [**gumtree_list_markets**](GumtreeApi.md#gumtree_list_markets) | **GET** /v1/gumtree/markets | List markets |
| [**gumtree_location_suggestions**](GumtreeApi.md#gumtree_location_suggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions |
| [**gumtree_search_listings**](GumtreeApi.md#gumtree_search_listings) | **GET** /v1/gumtree/search | Search listings |
| [**gumtree_search_suggestions**](GumtreeApi.md#gumtree_search_suggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions |


## gumtree_get_listing

> Object gumtree_get_listing(listing_id, opts)

Get listing

Full listing — description, attributes, images, seller, similar listings.

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

api_instance = ScrapeBadger::GumtreeApi.new
listing_id = 'listing_id_example' # String | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one)
opts = {
  market: 'uk', # String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get listing
  result = api_instance.gumtree_get_listing(listing_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_listing: #{e}"
end
```

#### Using the gumtree_get_listing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_get_listing_with_http_info(listing_id, opts)

```ruby
begin
  # Get listing
  data, status_code, headers = api_instance.gumtree_get_listing_with_http_info(listing_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_listing_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **listing_id** | **String** | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) |  |
| **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional][default to &#39;uk&#39;] |
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


## gumtree_get_search_filters

> Object gumtree_get_search_filters(opts)

Get search filters

Filters, sort orders and radius options for a category, with live counts.  Feed a `key` and a `value` back into `/search` as `filters=key:value`.

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

api_instance = ScrapeBadger::GumtreeApi.new
opts = {
  category: 'category_example', # String | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'.
  location: 'location_example', # String | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country.
  query: 'query_example', # String | Optional keywords to scope the counts
  filters: 'filters_example', # String | za only: filters already applied (e.g. 'ma:toyota' to list Toyota models)
  market: 'uk', # String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get search filters
  result = api_instance.gumtree_get_search_filters(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_search_filters: #{e}"
end
```

#### Using the gumtree_get_search_filters_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_get_search_filters_with_http_info(opts)

```ruby
begin
  # Get search filters
  data, status_code, headers = api_instance.gumtree_get_search_filters_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_search_filters_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category** | **String** | uk: category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;, &#39;bicycles&#39;. au/za: numeric category id, e.g. &#39;18320&#39; (au cars) or &#39;9077&#39; (za cars). Use /categories to browse the tree. Default &#39;all&#39;. | [optional][default to &#39;all&#39;] |
| **location** | **String** | uk: location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). au/za: numeric location id, e.g. &#39;3003435&#39; (au Sydney) or &#39;3100003&#39; (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. | [optional] |
| **query** | **String** | Optional keywords to scope the counts | [optional] |
| **filters** | **String** | za only: filters already applied (e.g. &#39;ma:toyota&#39; to list Toyota models) | [optional] |
| **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional][default to &#39;uk&#39;] |
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


## gumtree_get_seller_listings

> Object gumtree_get_seller_listings(listing_id, opts)

Get seller listings

Every live listing by the seller of the given listing.

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

api_instance = ScrapeBadger::GumtreeApi.new
listing_id = 'listing_id_example' # String | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one)
opts = {
  page: 56, # Integer | 
  market: 'uk', # String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get seller listings
  result = api_instance.gumtree_get_seller_listings(listing_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_seller_listings: #{e}"
end
```

#### Using the gumtree_get_seller_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_get_seller_listings_with_http_info(listing_id, opts)

```ruby
begin
  # Get seller listings
  data, status_code, headers = api_instance.gumtree_get_seller_listings_with_http_info(listing_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_seller_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **listing_id** | **String** | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) |  |
| **page** | **Integer** |  | [optional][default to 1] |
| **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional][default to &#39;uk&#39;] |
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


## gumtree_gumtree_scraper_health_check

> Object gumtree_gumtree_scraper_health_check

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::GumtreeApi.new

begin
  # Gumtree scraper health check
  result = api_instance.gumtree_gumtree_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_gumtree_scraper_health_check: #{e}"
end
```

#### Using the gumtree_gumtree_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_gumtree_scraper_health_check_with_http_info

```ruby
begin
  # Gumtree scraper health check
  data, status_code, headers = api_instance.gumtree_gumtree_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_gumtree_scraper_health_check_with_http_info: #{e}"
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


## gumtree_gumtree_scraper_health_check_head

> Object gumtree_gumtree_scraper_health_check_head

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::GumtreeApi.new

begin
  # Gumtree scraper health check
  result = api_instance.gumtree_gumtree_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_gumtree_scraper_health_check_head: #{e}"
end
```

#### Using the gumtree_gumtree_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_gumtree_scraper_health_check_head_with_http_info

```ruby
begin
  # Gumtree scraper health check
  data, status_code, headers = api_instance.gumtree_gumtree_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_gumtree_scraper_health_check_head_with_http_info: #{e}"
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


## gumtree_list_categories

> Object gumtree_list_categories(opts)

List categories

Browse Gumtree's category tree.  A node's `slug` (uk) or `id` (au/za) is the `/search` category.

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

api_instance = ScrapeBadger::GumtreeApi.new
opts = {
  parent_id: 56, # Integer | Category id to list the children of (default: all)
  market: 'uk', # String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # List categories
  result = api_instance.gumtree_list_categories(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_categories: #{e}"
end
```

#### Using the gumtree_list_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_list_categories_with_http_info(opts)

```ruby
begin
  # List categories
  data, status_code, headers = api_instance.gumtree_list_categories_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **parent_id** | **Integer** | Category id to list the children of (default: all) | [optional] |
| **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional][default to &#39;uk&#39;] |
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


## gumtree_list_locations

> Object gumtree_list_locations(opts)

List locations

Browse Gumtree's location tree.  uk: UK -> nations -> counties -> towns. au: states -> regions -> areas, each with its live ad count. za: provinces -> towns.

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

api_instance = ScrapeBadger::GumtreeApi.new
opts = {
  parent_id: 56, # Integer | Location id to list the children of (default: the whole country)
  market: 'uk', # String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # List locations
  result = api_instance.gumtree_list_locations(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_locations: #{e}"
end
```

#### Using the gumtree_list_locations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_list_locations_with_http_info(opts)

```ruby
begin
  # List locations
  data, status_code, headers = api_instance.gumtree_list_locations_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_locations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **parent_id** | **Integer** | Location id to list the children of (default: the whole country) | [optional] |
| **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional][default to &#39;uk&#39;] |
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


## gumtree_list_markets

> Object gumtree_list_markets(opts)

List markets

The Gumtree sites this API covers (uk, au, za) with currency and id formats.

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

api_instance = ScrapeBadger::GumtreeApi.new
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
  result = api_instance.gumtree_list_markets(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_markets: #{e}"
end
```

#### Using the gumtree_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_list_markets_with_http_info(opts)

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.gumtree_list_markets_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_markets_with_http_info: #{e}"
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


## gumtree_location_suggestions

> Object gumtree_location_suggestions(query, opts)

Location suggestions

Resolve a place name or postcode to Gumtree location ids (uk: with coordinates).  The `id` (au/za) or `name` (uk) is what `/search` takes as `location`.

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

api_instance = ScrapeBadger::GumtreeApi.new
query = 'query_example' # String | Town, area or postcode prefix, e.g. 'manch' or 'SW1A'
opts = {
  market: 'uk', # String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Location suggestions
  result = api_instance.gumtree_location_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_location_suggestions: #{e}"
end
```

#### Using the gumtree_location_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_location_suggestions_with_http_info(query, opts)

```ruby
begin
  # Location suggestions
  data, status_code, headers = api_instance.gumtree_location_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_location_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Town, area or postcode prefix, e.g. &#39;manch&#39; or &#39;SW1A&#39; |  |
| **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional][default to &#39;uk&#39;] |
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


## gumtree_search_listings

> Object gumtree_search_listings(opts)

Search listings

Search Gumtree listings in the UK, Australia or South Africa.  Up to 50 pages. Page size: uk 25, au 24 (plus up to 6 featured top ads), za 20.

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

api_instance = ScrapeBadger::GumtreeApi.new
opts = {
  query: 'query_example', # String | Search keywords, e.g. 'mountain bike'
  category: 'category_example', # String | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'.
  location: 'location_example', # String | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country.
  distance: 8.14, # Float | Radius around `location`: miles (uk) or km (au). Not offered by za.
  min_price: 56, # Integer | Minimum price in the market's currency (uk: needs a category, not 'all')
  max_price: 56, # Integer | Maximum price in the market's currency (uk: needs a category, not 'all')
  sort: 'relevance', # String | Result ordering (default relevance). 'distance' needs uk, or au with a location.
  seller_type: 'private', # String | uk/za: 'trade' covers dealers, agencies and recruiters. au: not supported — use a category filter such as 'cars.forsaleby_s:ownr'.
  urgent_only: true, # Boolean | uk only: only ads marked urgent
  with_photos: true, # Boolean | uk only: only ads with photos
  filters: 'filters_example', # String | Category-specific filters as comma-separated key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol,min_vehicle_mileage:10000' (uk), 'cars.carmake_s:toyota,cars.forsaleby_s:ownr' (au) or 'ma:toyota,fu:petrol,max_km:100000' (za). Range filters take min_<key>/max_<key>. Discover keys and values with /search/filters for the same market.
  page: 56, # Integer | 
  market: 'uk', # String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Search listings
  result = api_instance.gumtree_search_listings(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_search_listings: #{e}"
end
```

#### Using the gumtree_search_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_search_listings_with_http_info(opts)

```ruby
begin
  # Search listings
  data, status_code, headers = api_instance.gumtree_search_listings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_search_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;mountain bike&#39; | [optional] |
| **category** | **String** | uk: category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;, &#39;bicycles&#39;. au/za: numeric category id, e.g. &#39;18320&#39; (au cars) or &#39;9077&#39; (za cars). Use /categories to browse the tree. Default &#39;all&#39;. | [optional][default to &#39;all&#39;] |
| **location** | **String** | uk: location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). au/za: numeric location id, e.g. &#39;3003435&#39; (au Sydney) or &#39;3100003&#39; (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. | [optional] |
| **distance** | **Float** | Radius around &#x60;location&#x60;: miles (uk) or km (au). Not offered by za. | [optional] |
| **min_price** | **Integer** | Minimum price in the market&#39;s currency (uk: needs a category, not &#39;all&#39;) | [optional] |
| **max_price** | **Integer** | Maximum price in the market&#39;s currency (uk: needs a category, not &#39;all&#39;) | [optional] |
| **sort** | **String** | Result ordering (default relevance). &#39;distance&#39; needs uk, or au with a location. | [optional] |
| **seller_type** | **String** | uk/za: &#39;trade&#39; covers dealers, agencies and recruiters. au: not supported — use a category filter such as &#39;cars.forsaleby_s:ownr&#39;. | [optional] |
| **urgent_only** | **Boolean** | uk only: only ads marked urgent | [optional][default to false] |
| **with_photos** | **Boolean** | uk only: only ads with photos | [optional][default to false] |
| **filters** | **String** | Category-specific filters as comma-separated key:value pairs, e.g. &#39;vehicle_make:bmw,vehicle_fuel_type:petrol,min_vehicle_mileage:10000&#39; (uk), &#39;cars.carmake_s:toyota,cars.forsaleby_s:ownr&#39; (au) or &#39;ma:toyota,fu:petrol,max_km:100000&#39; (za). Range filters take min_&lt;key&gt;/max_&lt;key&gt;. Discover keys and values with /search/filters for the same market. | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional][default to &#39;uk&#39;] |
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


## gumtree_search_suggestions

> Object gumtree_search_suggestions(query, opts)

Search suggestions

Gumtree search-box keyword suggestions with their categories.

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

api_instance = ScrapeBadger::GumtreeApi.new
query = 'query_example' # String | Partial search term, e.g. 'iph'
opts = {
  market: 'uk', # String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Search suggestions
  result = api_instance.gumtree_search_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_search_suggestions: #{e}"
end
```

#### Using the gumtree_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_search_suggestions_with_http_info(query, opts)

```ruby
begin
  # Search suggestions
  data, status_code, headers = api_instance.gumtree_search_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial search term, e.g. &#39;iph&#39; |  |
| **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional][default to &#39;uk&#39;] |
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

