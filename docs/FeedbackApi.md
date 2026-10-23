# ScrapeBadger::FeedbackApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**feedback_report_a_bug_or_send_feedback**](FeedbackApi.md#feedback_report_a_bug_or_send_feedback) | **POST** /v1/feedback | Report a bug or send feedback |


## feedback_report_a_bug_or_send_feedback

> Object feedback_report_a_bug_or_send_feedback(feedback_request)

Report a bug or send feedback

File a bug (wrong/empty result for valid input, misleading error, price mismatch) or feedback (an API or field you needed and couldn't find). Free, never billed. Pass the failing call's X-Request-ID so we can find it.

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

api_instance = ScrapeBadger::FeedbackApi.new
feedback_request = ScrapeBadger::FeedbackRequest.new({type: 'bug', summary: 'summary_example'}) # FeedbackRequest | 

begin
  # Report a bug or send feedback
  result = api_instance.feedback_report_a_bug_or_send_feedback(feedback_request)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FeedbackApi->feedback_report_a_bug_or_send_feedback: #{e}"
end
```

#### Using the feedback_report_a_bug_or_send_feedback_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> feedback_report_a_bug_or_send_feedback_with_http_info(feedback_request)

```ruby
begin
  # Report a bug or send feedback
  data, status_code, headers = api_instance.feedback_report_a_bug_or_send_feedback_with_http_info(feedback_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling FeedbackApi->feedback_report_a_bug_or_send_feedback_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **feedback_request** | [**FeedbackRequest**](FeedbackRequest.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

