# ScrapeBadger::AccountApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**account_get_account_info**](AccountApi.md#account_get_account_info) | **GET** /v1/account/me | Get account info |


## account_get_account_info

> <AccountInfo> account_get_account_info

Get account info

Get account details for the authenticated API key.  Returns credit balances, tier, rate limit, and subscription details. No credits are deducted for this call.

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

api_instance = ScrapeBadger::AccountApi.new

begin
  # Get account info
  result = api_instance.account_get_account_info
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AccountApi->account_get_account_info: #{e}"
end
```

#### Using the account_get_account_info_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AccountInfo>, Integer, Hash)> account_get_account_info_with_http_info

```ruby
begin
  # Get account info
  data, status_code, headers = api_instance.account_get_account_info_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AccountInfo>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AccountApi->account_get_account_info_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AccountInfo**](AccountInfo.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

