# ScrapeBadger::RequestsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**requests_callback_status**](RequestsApi.md#requests_callback_status) | **GET** /v1/requests/{request_id}/callback | Callback status |
| [**requests_poll_an_async_request**](RequestsApi.md#requests_poll_an_async_request) | **GET** /v1/requests/{request_id} | Poll an async request |


## requests_callback_status

> <AsyncCallbackStatus> requests_callback_status(request_id)

Callback status

Webhook delivery state of a call submitted with `X-Callback-URL` / `callback_url`: kept for 24 h. Free. `404 callback_not_found` for a request without a callback, of another account, or older than 24 h.

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

api_instance = ScrapeBadger::RequestsApi.new
request_id = 'request_id_example' # String | 

begin
  # Callback status
  result = api_instance.requests_callback_status(request_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RequestsApi->requests_callback_status: #{e}"
end
```

#### Using the requests_callback_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AsyncCallbackStatus>, Integer, Hash)> requests_callback_status_with_http_info(request_id)

```ruby
begin
  # Callback status
  data, status_code, headers = api_instance.requests_callback_status_with_http_info(request_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AsyncCallbackStatus>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RequestsApi->requests_callback_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **request_id** | **String** |  |  |

### Return type

[**AsyncCallbackStatus**](AsyncCallbackStatus.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## requests_poll_an_async_request

> Object requests_poll_an_async_request(request_id)

Poll an async request

Status or final response of a call made with ``Prefer: respond-async``. While it runs: 202. When done: the original status, headers and body.  The final response carries `X-Callback-Status`, `X-Callback-Attempts` and `X-Callback-Error` for a call submitted with a callback; while it runs, the `202` body has a `callback` object. Full delivery state: `GET /v1/requests/{request_id}/callback`.

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

api_instance = ScrapeBadger::RequestsApi.new
request_id = 'request_id_example' # String | 

begin
  # Poll an async request
  result = api_instance.requests_poll_an_async_request(request_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RequestsApi->requests_poll_an_async_request: #{e}"
end
```

#### Using the requests_poll_an_async_request_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> requests_poll_an_async_request_with_http_info(request_id)

```ruby
begin
  # Poll an async request
  data, status_code, headers = api_instance.requests_poll_an_async_request_with_http_info(request_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RequestsApi->requests_poll_an_async_request_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **request_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

