# ScrapeBadger::AsyncCallbackStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **request_id** | **String** |  |  |
| **state** | **String** | &#x60;pending&#x60;: the call is still running. &#x60;delivering&#x60;: an attempt is under way or the next retry is due at &#x60;next_attempt_at&#x60;. &#x60;delivered&#x60;: the endpoint answered 2xx. &#x60;failed&#x60;: every attempt failed, a final status (not 408/429/5xx) came back, or a gateway restart interrupted the delivery (&#x60;last_error&#x60; \&quot;interrupted (gateway restart)\&quot;). |  |
| **attempts** | **Integer** |  |  |
| **last_status** | **Integer** |  | [optional] |
| **last_error** | **String** |  | [optional] |
| **next_attempt_at** | **Integer** |  | [optional] |
| **delivered_at** | **Integer** |  | [optional] |
| **callback_host** | **String** | Host of the callback URL only (never its path or query). |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::AsyncCallbackStatus.new(
  request_id: null,
  state: null,
  attempts: null,
  last_status: null,
  last_error: null,
  next_attempt_at: null,
  delivered_at: null,
  callback_host: null
)
```

