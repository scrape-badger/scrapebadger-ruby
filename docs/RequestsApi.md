# ScrapeBadger::RequestsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**requests_poll_an_async_request**](RequestsApi.md#requests_poll_an_async_request) | **GET** /v1/requests/{request_id} | Poll an async request |


## requests_poll_an_async_request

> Object requests_poll_an_async_request(request_id)

Poll an async request

Status or final response of a call made with ``Prefer: respond-async``. While it runs: 202. When done: the original status, headers and body.

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

