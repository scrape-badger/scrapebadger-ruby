# ScrapeBadger::BatchApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**batch_submit_a_batch_of_async_requests**](BatchApi.md#batch_submit_a_batch_of_async_requests) | **POST** /v1/batch | Submit a batch of async requests |


## batch_submit_a_batch_of_async_requests

> Object batch_submit_a_batch_of_async_requests(batch_request)

Submit a batch of async requests

Submit up to 100 GET reads in one call. Each item runs as its own ``Prefer: respond-async`` request under this key, with the same auth, credit check, rate limit and billing as if it were sent alone, and returns a request_id to poll (or a webhook to ``callback_url``). At most 10 items of a batch run at the same time. Submitting is free; each item bills as it runs. Items are checked against the spendable balance first, at the endpoint's base price, so a batch never starts more than the account can pay for.

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

api_instance = ScrapeBadger::BatchApi.new
batch_request = ScrapeBadger::BatchRequest.new({requests: [ScrapeBadger::BatchItem.new({path: 'path_example'})]}) # BatchRequest | 

begin
  # Submit a batch of async requests
  result = api_instance.batch_submit_a_batch_of_async_requests(batch_request)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BatchApi->batch_submit_a_batch_of_async_requests: #{e}"
end
```

#### Using the batch_submit_a_batch_of_async_requests_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> batch_submit_a_batch_of_async_requests_with_http_info(batch_request)

```ruby
begin
  # Submit a batch of async requests
  data, status_code, headers = api_instance.batch_submit_a_batch_of_async_requests_with_http_info(batch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BatchApi->batch_submit_a_batch_of_async_requests_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **batch_request** | [**BatchRequest**](BatchRequest.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

