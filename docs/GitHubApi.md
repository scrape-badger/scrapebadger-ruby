# ScrapeBadger::GitHubApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**github_get_profile**](GitHubApi.md#github_get_profile) | **GET** /v1/github/profiles/{username} | Get profile |


## github_get_profile

> <GitHubProfileResponse> github_get_profile(username, opts)

Get profile

Public user or organization profile, pins/popular repositories, README and contributions.  The overview preserves GitHub's public website sections, including organization-specific metadata. Compact displayed counts are approximate and marked with *_approximate. Unavailable or blocked data is an unbilled error, never an empty success.

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

api_instance = ScrapeBadger::GitHubApi.new
username = 'username_example' # String | 
opts = {
  tab: 'overview', # String | Profile section; stars is available for users only
  year: 56, # Integer | Overview only: 1970 through the current UTC year; activity is December or current month
  page: 56, # Integer | Repositories only: page number, 30 rows per page
  next_page_token: 'next_page_token_example' # String | Stars only: previous pagination.next_page_token
}

begin
  # Get profile
  result = api_instance.github_get_profile(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GitHubApi->github_get_profile: #{e}"
end
```

#### Using the github_get_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GitHubProfileResponse>, Integer, Hash)> github_get_profile_with_http_info(username, opts)

```ruby
begin
  # Get profile
  data, status_code, headers = api_instance.github_get_profile_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GitHubProfileResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GitHubApi->github_get_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **tab** | **String** | Profile section; stars is available for users only | [optional][default to &#39;overview&#39;] |
| **year** | **Integer** | Overview only: 1970 through the current UTC year; activity is December or current month | [optional] |
| **page** | **Integer** | Repositories only: page number, 30 rows per page | [optional] |
| **next_page_token** | **String** | Stars only: previous pagination.next_page_token | [optional] |

### Return type

[**GitHubProfileResponse**](GitHubProfileResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

