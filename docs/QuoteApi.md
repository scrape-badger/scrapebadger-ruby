# ScrapeBadger::QuoteApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**quote_quote_a_call**](QuoteApi.md#quote_quote_a_call) | **POST** /v1/quote | Quote a call |


## quote_quote_a_call

> Object quote_quote_a_call(quote_request)

Quote a call

What a call would cost (credits and USD), whether its parameters are valid, and how long it usually takes. Free: nothing runs and nothing is charged.

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

api_instance = ScrapeBadger::QuoteApi.new
quote_request = ScrapeBadger::QuoteRequest.new({path: 'path_example'}) # QuoteRequest | 

begin
  # Quote a call
  result = api_instance.quote_quote_a_call(quote_request)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling QuoteApi->quote_quote_a_call: #{e}"
end
```

#### Using the quote_quote_a_call_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> quote_quote_a_call_with_http_info(quote_request)

```ruby
begin
  # Quote a call
  data, status_code, headers = api_instance.quote_quote_a_call_with_http_info(quote_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling QuoteApi->quote_quote_a_call_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quote_request** | [**QuoteRequest**](QuoteRequest.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

