# ScrapeBadger::ResultsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**results_re_read_a_result_removed**](ResultsApi.md#results_re_read_a_result_removed) | **GET** /v1/results/{result_id} | Re-read a result (removed) |


## results_re_read_a_result_removed

> Object results_re_read_a_result_removed(result_id)

Re-read a result (removed)

Removed (SCR-396): ScrapeBadger no longer stores results, so there is nothing to re-read. Always 410. Narrow a call with _jq / _fields / _max_items instead.

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
  # Re-read a result (removed)
  result = api_instance.results_re_read_a_result_removed(result_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ResultsApi->results_re_read_a_result_removed: #{e}"
end
```

#### Using the results_re_read_a_result_removed_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> results_re_read_a_result_removed_with_http_info(result_id)

```ruby
begin
  # Re-read a result (removed)
  data, status_code, headers = api_instance.results_re_read_a_result_removed_with_http_info(result_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling ResultsApi->results_re_read_a_result_removed_with_http_info: #{e}"
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

