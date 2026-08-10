# ScrapeBadger::WebhookTestResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  |  |
| **status_code** | **Integer** |  | [optional] |
| **response_time_ms** | **Float** | Round-trip time in milliseconds |  |
| **error** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::WebhookTestResponse.new(
  success: null,
  status_code: null,
  response_time_ms: null,
  error: null
)
```

