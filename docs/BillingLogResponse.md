# ScrapeBadger::BillingLogResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **monitor_id** | **String** |  |  |
| **monitor_name** | **String** |  |  |
| **billed_at** | **Time** |  |  |
| **num_accounts** | **Integer** |  |  |
| **credits_deducted** | **Float** |  |  |
| **tier_label** | **String** |  |  |
| **rate_applied** | **Float** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::BillingLogResponse.new(
  id: null,
  monitor_id: null,
  monitor_name: null,
  billed_at: null,
  num_accounts: null,
  credits_deducted: null,
  tier_label: null,
  rate_applied: null
)
```

