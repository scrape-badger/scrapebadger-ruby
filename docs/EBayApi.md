# ScrapeBadger::EBayApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**ebay_browse_a_category**](EBayApi.md#ebay_browse_a_category) | **GET** /v1/ebay/categories/{category_id}/items | Browse a category |
| [**ebay_completed_sold_listings**](EBayApi.md#ebay_completed_sold_listings) | **GET** /v1/ebay/completed | Completed / sold listings |
| [**ebay_ebay_scraper_health_check**](EBayApi.md#ebay_ebay_scraper_health_check) | **GET** /v1/ebay/health | eBay scraper health check |
| [**ebay_ebay_scraper_health_check_head**](EBayApi.md#ebay_ebay_scraper_health_check_head) | **HEAD** /v1/ebay/health | eBay scraper health check |
| [**ebay_get_item_detail**](EBayApi.md#ebay_get_item_detail) | **GET** /v1/ebay/items/{item_id} | Get item detail |
| [**ebay_get_item_reviews**](EBayApi.md#ebay_get_item_reviews) | **GET** /v1/ebay/items/{item_id}/reviews | Get item reviews |
| [**ebay_get_seller_feedback**](EBayApi.md#ebay_get_seller_feedback) | **GET** /v1/ebay/sellers/{username}/feedback | Get seller feedback |
| [**ebay_get_seller_listings**](EBayApi.md#ebay_get_seller_listings) | **GET** /v1/ebay/sellers/{username}/items | Get seller listings |
| [**ebay_get_seller_profile**](EBayApi.md#ebay_get_seller_profile) | **GET** /v1/ebay/sellers/{username} | Get seller profile |
| [**ebay_keyword_suggestions**](EBayApi.md#ebay_keyword_suggestions) | **GET** /v1/ebay/autocomplete | Keyword suggestions |
| [**ebay_list_categories**](EBayApi.md#ebay_list_categories) | **GET** /v1/ebay/categories | List categories |
| [**ebay_list_markets**](EBayApi.md#ebay_list_markets) | **GET** /v1/ebay/markets | List markets |
| [**ebay_search_by_image**](EBayApi.md#ebay_search_by_image) | **POST** /v1/ebay/search/by-image | Search by image |
| [**ebay_search_listings**](EBayApi.md#ebay_search_listings) | **GET** /v1/ebay/search | Search listings |


## ebay_browse_a_category

> Object ebay_browse_a_category(category_id, opts)

Browse a category

List active listings within an eBay category.

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

api_instance = ScrapeBadger::EBayApi.new
category_id = 'category_id_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  page: 56, # Integer | 
  per_page: 56, # Integer | 
  sort_by: 'sort_by_example', # String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Browse a category
  result = api_instance.ebay_browse_a_category(category_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_browse_a_category: #{e}"
end
```

#### Using the ebay_browse_a_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_browse_a_category_with_http_info(category_id, opts)

```ruby
begin
  # Browse a category
  data, status_code, headers = api_instance.ebay_browse_a_category_with_http_info(category_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_browse_a_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** |  | [optional] |
| **sort_by** | **String** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional][default to &#39;best_match&#39;] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
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


## ebay_completed_sold_listings

> Object ebay_completed_sold_listings(opts)

Completed / sold listings

Search completed/sold listings — eBay's sold-price history.  Pass ``query``, ``seller`` or both. ``seller`` alone returns everything that seller sold, page by page, with no keyword needed.  eBay pads a short result set with \"results matching fewer words\" and counts only the exact ones in ``pagination.total_results``. Results come back in eBay's own ranking order with the exact matches first, and each one carries ``exact_match`` (true/false) so a price series can be built without parsing titles. An empty ``results`` with ``total_results: 0`` is eBay's own answer and costs 0 credits — a fetch failure is never a 200.  ``price`` is what the listing sold for, including the market's buyer-protection fee, as a local buyer sees it. It is ``null`` on one shape: an auction that also accepted offers (``bids`` set). eBay's sold index answers those with either the listing's start/Buy-It-Now price or the price it sold at, varying between identical requests with nothing to say which, so no number there is trustworthy — ``/v1/ebay/items/{item_id}`` carries the winning bid for them (before the fee). A listing that closed purely on an accepted Best Offer prices normally: eBay's sold index carries the listed price for it, not the accepted amount, so ``price`` is the listed one. ``/v1/ebay/items/{item_id}`` carries the accepted amount where eBay's item page publishes it (``best_offer_accepted``, ``price``, ``original_price``).

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

api_instance = ScrapeBadger::EBayApi.new
opts = {
  query: 'query_example', # String | Search keywords. Optional when `seller` is set.
  seller: 'seller_example', # String | Only this seller's sold listings (eBay username). Works without `query`.
  domain: 'domain_example', # String | Marketplace domain (com, co.uk, de …)
  category_id: 'category_id_example', # String | Restrict to a category id
  page: 56, # Integer | 
  per_page: 56, # Integer | 60, 120 or 240
  sort_by: 'sort_by_example', # String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
  condition: 'condition_example', # String | new|open_box|refurbished|used|for_parts|graded|ungraded
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  location: 'location_example', # String | domestic|worldwide
  language: 'language_example', # String | english|japanese|chinese|korean
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Completed / sold listings
  result = api_instance.ebay_completed_sold_listings(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_completed_sold_listings: #{e}"
end
```

#### Using the ebay_completed_sold_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_completed_sold_listings_with_http_info(opts)

```ruby
begin
  # Completed / sold listings
  data, status_code, headers = api_instance.ebay_completed_sold_listings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_completed_sold_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords. Optional when &#x60;seller&#x60; is set. | [optional] |
| **seller** | **String** | Only this seller&#39;s sold listings (eBay username). Works without &#x60;query&#x60;. | [optional] |
| **domain** | **String** | Marketplace domain (com, co.uk, de …) | [optional][default to &#39;com&#39;] |
| **category_id** | **String** | Restrict to a category id | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** | 60, 120 or 240 | [optional] |
| **sort_by** | **String** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional][default to &#39;best_match&#39;] |
| **condition** | **String** | new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **location** | **String** | domestic|worldwide | [optional] |
| **language** | **String** | english|japanese|chinese|korean | [optional] |
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


## ebay_ebay_scraper_health_check

> Object ebay_ebay_scraper_health_check

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::EBayApi.new

begin
  # eBay scraper health check
  result = api_instance.ebay_ebay_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_ebay_scraper_health_check: #{e}"
end
```

#### Using the ebay_ebay_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_ebay_scraper_health_check_with_http_info

```ruby
begin
  # eBay scraper health check
  data, status_code, headers = api_instance.ebay_ebay_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_ebay_scraper_health_check_with_http_info: #{e}"
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


## ebay_ebay_scraper_health_check_head

> Object ebay_ebay_scraper_health_check_head

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::EBayApi.new

begin
  # eBay scraper health check
  result = api_instance.ebay_ebay_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_ebay_scraper_health_check_head: #{e}"
end
```

#### Using the ebay_ebay_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_ebay_scraper_health_check_head_with_http_info

```ruby
begin
  # eBay scraper health check
  data, status_code, headers = api_instance.ebay_ebay_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_ebay_scraper_health_check_head_with_http_info: #{e}"
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


## ebay_get_item_detail

> Object ebay_get_item_detail(item_id, opts)

Get item detail

Get a single eBay listing's full detail.  ``price`` is the price the listing's buy box shows. On a closed listing, ``is_sold`` says it carries eBay's \"Sold\" label rather than \"Ended\", and ``best_offer_accepted`` says it sold through an accepted Best Offer. eBay publishes the accepted amount on most such listings: then ``price`` is that amount, and ``original_price`` and ``buy_it_now_price`` are the listed price it was accepted against. Where eBay only strikes the listed price through, ``price`` stays the listed price and ``original_price`` is null, so ``best_offer_accepted`` with a null ``original_price`` means \"sold below ``price``, amount not published on this read\". On a listing from another eBay site the accepted amount is converted to the marketplace's currency at the rate eBay applied to the listed price on the same page; ``price.raw`` keeps it as eBay rendered it (\"US $300.00\").

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

api_instance = ScrapeBadger::EBayApi.new
item_id = 'item_id_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get item detail
  result = api_instance.ebay_get_item_detail(item_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_item_detail: #{e}"
end
```

#### Using the ebay_get_item_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_item_detail_with_http_info(item_id, opts)

```ruby
begin
  # Get item detail
  data, status_code, headers = api_instance.ebay_get_item_detail_with_http_info(item_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_item_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
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


## ebay_get_item_reviews

> Object ebay_get_item_reviews(item_id, opts)

Get item reviews

Get catalog product reviews shown on an eBay listing.

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

api_instance = ScrapeBadger::EBayApi.new
item_id = 'item_id_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  page: 56, # Integer | 
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get item reviews
  result = api_instance.ebay_get_item_reviews(item_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_item_reviews: #{e}"
end
```

#### Using the ebay_get_item_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_item_reviews_with_http_info(item_id, opts)

```ruby
begin
  # Get item reviews
  data, status_code, headers = api_instance.ebay_get_item_reviews_with_http_info(item_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_item_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
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


## ebay_get_seller_feedback

> Object ebay_get_seller_feedback(username, opts)

Get seller feedback

Get a seller's recent feedback comments.

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

api_instance = ScrapeBadger::EBayApi.new
username = 'username_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  page: 56, # Integer | 
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get seller feedback
  result = api_instance.ebay_get_seller_feedback(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_feedback: #{e}"
end
```

#### Using the ebay_get_seller_feedback_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_seller_feedback_with_http_info(username, opts)

```ruby
begin
  # Get seller feedback
  data, status_code, headers = api_instance.ebay_get_seller_feedback_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_feedback_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **page** | **Integer** |  | [optional][default to 1] |
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


## ebay_get_seller_listings

> Object ebay_get_seller_listings(username, opts)

Get seller listings

List the active listings of a single eBay seller.

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

api_instance = ScrapeBadger::EBayApi.new
username = 'username_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  query: 'query_example', # String | 
  page: 56, # Integer | 
  per_page: 56, # Integer | 
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
  result = api_instance.ebay_get_seller_listings(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_listings: #{e}"
end
```

#### Using the ebay_get_seller_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_seller_listings_with_http_info(username, opts)

```ruby
begin
  # Get seller listings
  data, status_code, headers = api_instance.ebay_get_seller_listings_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
| **query** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** |  | [optional] |
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


## ebay_get_seller_profile

> Object ebay_get_seller_profile(username, opts)

Get seller profile

Get an eBay seller's public profile.

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

api_instance = ScrapeBadger::EBayApi.new
username = 'username_example' # String | 
opts = {
  domain: 'domain_example', # String | 
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Get seller profile
  result = api_instance.ebay_get_seller_profile(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_profile: #{e}"
end
```

#### Using the ebay_get_seller_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_get_seller_profile_with_http_info(username, opts)

```ruby
begin
  # Get seller profile
  data, status_code, headers = api_instance.ebay_get_seller_profile_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_get_seller_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
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


## ebay_keyword_suggestions

> Object ebay_keyword_suggestions(query, opts)

Keyword suggestions

Return eBay keyword autocomplete suggestions.

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

api_instance = ScrapeBadger::EBayApi.new
query = 'query_example' # String | Partial query prefix
opts = {
  domain: 'domain_example', # String | 
  prefer: 'respond-async, wait=25', # String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait.
  x_callback_url: 'x_callback_url_example', # String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`.
  idempotency_key: 'idempotency_key_example', # String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`.
  async: true, # Boolean | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper.
  async_wait: 56, # Integer | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper.
  callback_url: 'callback_url_example', # String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper.
  idempotency_key2: 'idempotency_key_example' # String | Query form of `Idempotency-Key`. Not sent to the scraper.
}

begin
  # Keyword suggestions
  result = api_instance.ebay_keyword_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_keyword_suggestions: #{e}"
end
```

#### Using the ebay_keyword_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_keyword_suggestions_with_http_info(query, opts)

```ruby
begin
  # Keyword suggestions
  data, status_code, headers = api_instance.ebay_keyword_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_keyword_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial query prefix |  |
| **domain** | **String** |  | [optional][default to &#39;com&#39;] |
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


## ebay_list_categories

> Object ebay_list_categories(opts)

List categories

List eBay's top-level category ids.

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

api_instance = ScrapeBadger::EBayApi.new
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
  # List categories
  result = api_instance.ebay_list_categories(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_list_categories: #{e}"
end
```

#### Using the ebay_list_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_list_categories_with_http_info(opts)

```ruby
begin
  # List categories
  data, status_code, headers = api_instance.ebay_list_categories_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_list_categories_with_http_info: #{e}"
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


## ebay_list_markets

> Object ebay_list_markets(opts)

List markets

List all supported eBay marketplaces.

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

api_instance = ScrapeBadger::EBayApi.new
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
  result = api_instance.ebay_list_markets(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_list_markets: #{e}"
end
```

#### Using the ebay_list_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_list_markets_with_http_info(opts)

```ruby
begin
  # List markets
  data, status_code, headers = api_instance.ebay_list_markets_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_list_markets_with_http_info: #{e}"
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


## ebay_search_by_image

> Object ebay_search_by_image(request_body, opts)

Search by image

Search active listings by image, the way eBay's camera icon does.  No ``sort_by``: eBay ignores it on a visual results page.

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

api_instance = ScrapeBadger::EBayApi.new
request_body = { key: 3.56} # Hash<String, Object> | 
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
  # Search by image
  result = api_instance.ebay_search_by_image(request_body, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_search_by_image: #{e}"
end
```

#### Using the ebay_search_by_image_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_search_by_image_with_http_info(request_body, opts)

```ruby
begin
  # Search by image
  data, status_code, headers = api_instance.ebay_search_by_image_with_http_info(request_body, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_search_by_image_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **request_body** | [**Hash&lt;String, Object&gt;**](Object.md) |  |  |
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

- **Content-Type**: application/json
- **Accept**: application/json


## ebay_search_listings

> Object ebay_search_listings(query, opts)

Search listings

Search an eBay marketplace for active listings.

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

api_instance = ScrapeBadger::EBayApi.new
query = 'query_example' # String | Search keywords
opts = {
  domain: 'domain_example', # String | Marketplace domain (com, co.uk, de …)
  category_id: 'category_id_example', # String | Restrict to a category id
  page: 56, # Integer | 
  per_page: 56, # Integer | 60, 120 or 240
  sort_by: 'sort_by_example', # String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
  condition: 'condition_example', # String | new|open_box|refurbished|used|for_parts|graded|ungraded
  buying_format: 'buying_format_example', # String | auction|buy_it_now|best_offer
  min_price: 8.14, # Float | 
  max_price: 8.14, # Float | 
  free_shipping: true, # Boolean | 
  location: 'location_example', # String | domestic|worldwide
  language: 'language_example', # String | english|japanese|chinese|korean
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
  result = api_instance.ebay_search_listings(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_search_listings: #{e}"
end
```

#### Using the ebay_search_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> ebay_search_listings_with_http_info(query, opts)

```ruby
begin
  # Search listings
  data, status_code, headers = api_instance.ebay_search_listings_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling EBayApi->ebay_search_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords |  |
| **domain** | **String** | Marketplace domain (com, co.uk, de …) | [optional][default to &#39;com&#39;] |
| **category_id** | **String** | Restrict to a category id | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **per_page** | **Integer** | 60, 120 or 240 | [optional] |
| **sort_by** | **String** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional][default to &#39;best_match&#39;] |
| **condition** | **String** | new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] |
| **buying_format** | **String** | auction|buy_it_now|best_offer | [optional] |
| **min_price** | **Float** |  | [optional] |
| **max_price** | **Float** |  | [optional] |
| **free_shipping** | **Boolean** |  | [optional][default to false] |
| **location** | **String** | domestic|worldwide | [optional] |
| **language** | **String** | english|japanese|chinese|korean | [optional] |
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

