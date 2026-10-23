# ScrapeBadger::FeedbackRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **summary** | **String** |  |  |
| **details** | **String** |  | [optional] |
| **request_id** | **String** |  | [optional] |
| **endpoint** | **String** |  | [optional] |
| **contact** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::FeedbackRequest.new(
  type: null,
  summary: null,
  details: null,
  request_id: null,
  endpoint: null,
  contact: null
)
```

