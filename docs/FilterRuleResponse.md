# ScrapeBadger::FilterRuleResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **tag** | **String** |  |  |
| **query** | **String** |  |  |
| **interval_seconds** | **Float** |  |  |
| **max_results_per_poll** | **Integer** |  |  |
| **status** | **String** |  |  |
| **status_reason** | **String** |  |  |
| **webhook_url** | **String** |  |  |
| **webhook_secret_set** | **Boolean** |  |  |
| **total_credits_burned** | **Float** |  |  |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::FilterRuleResponse.new(
  id: null,
  tag: null,
  query: null,
  interval_seconds: null,
  max_results_per_poll: null,
  status: null,
  status_reason: null,
  webhook_url: null,
  webhook_secret_set: null,
  total_credits_burned: null,
  created_at: null,
  updated_at: null
)
```

