# ScrapeBadger::AsyncAccepted

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **request_id** | **String** |  |  |
| **status** | **String** |  |  |
| **retry_after_seconds** | **Integer** |  |  |
| **next_action** | [**AsyncAcceptedNextAction**](AsyncAcceptedNextAction.md) |  |  |
| **detail** | **String** |  | [optional] |
| **callback** | **Object** | Only on a poll of a call submitted with a callback: the delivery state so far (&#x60;status&#x60;, &#x60;attempts&#x60;, &#x60;last_error&#x60;). | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::AsyncAccepted.new(
  request_id: null,
  status: null,
  retry_after_seconds: 5,
  next_action: null,
  detail: null,
  callback: null
)
```

