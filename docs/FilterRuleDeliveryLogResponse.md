# ScrapeBadger::FilterRuleDeliveryLogResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **rule_id** | **String** |  |  |
| **rule_tag** | **String** |  |  |
| **tweet_id** | **String** |  |  |
| **author_username** | **String** |  |  |
| **tweet_text_preview** | **String** |  |  |
| **tweet_url** | **String** |  |  |
| **tweet_published_at** | **Time** |  |  |
| **detected_at** | **Time** |  |  |
| **latency_ms** | **Integer** |  |  |
| **latency_badge** | **String** |  |  |
| **delivery_status** | **String** |  |  |
| **webhook_status_code** | **Integer** |  |  |
| **webhook_attempts** | **Integer** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::FilterRuleDeliveryLogResponse.new(
  id: null,
  rule_id: null,
  rule_tag: null,
  tweet_id: null,
  author_username: null,
  tweet_text_preview: null,
  tweet_url: null,
  tweet_published_at: null,
  detected_at: null,
  latency_ms: null,
  latency_badge: null,
  delivery_status: null,
  webhook_status_code: null,
  webhook_attempts: null
)
```

