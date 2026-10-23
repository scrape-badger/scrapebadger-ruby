# ScrapeBadger::ResultsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**results_re_read_a_result**](ResultsApi.md#results_re_read_a_result) | **GET** /v1/results/{result_id} | Re-read a result |


## results_re_read_a_result

> Object results_re_read_a_result(result_id)

Re-read a result

Replay a billed result (X-Result-ID) for free for ~15 minutes, optionally trimmed with jq / fields / max_items / summary. Never re-run a paid call just to reshape it.

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

api_instance = ScrapeBadger::ResultsApi.new
result_id = 'result_id_example' # String | 

begin
  # Re-read a result
  result = api_instance.results_re_read_a_result(result_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ResultsApi->results_re_read_a_result: #{e}"
end
```

#### Using the results_re_read_a_result_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> results_re_read_a_result_with_http_info(result_id)

```ruby
begin
  # Re-read a result
  data, status_code, headers = api_instance.results_re_read_a_result_with_http_info(result_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ResultsApi->results_re_read_a_result_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **result_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

