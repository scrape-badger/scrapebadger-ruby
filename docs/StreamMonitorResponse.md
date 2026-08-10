# ScrapeBadger::StreamMonitorResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **name** | **String** |  |  |
| **usernames** | **Array&lt;String&gt;** |  |  |
| **status** | **String** |  |  |
| **status_reason** | **String** |  |  |
| **webhook_url** | **String** |  |  |
| **webhook_secret_set** | **Boolean** |  |  |
| **filter_types** | **Array&lt;String&gt;** |  |  |
| **credits_per_account_per_day** | **Float** |  |  |
| **estimated_credits_per_day** | **Float** |  |  |
| **pricing_tier** | **String** |  |  |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::StreamMonitorResponse.new(
  id: null,
  name: null,
  usernames: null,
  status: null,
  status_reason: null,
  webhook_url: null,
  webhook_secret_set: null,
  filter_types: null,
  credits_per_account_per_day: null,
  estimated_credits_per_day: null,
  pricing_tier: null,
  created_at: null,
  updated_at: null
)
```

