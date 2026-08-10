# ScrapeBadger::SubscriptionInfo

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **plan_code** | **String** |  |  |
| **plan_title** | **String** |  |  |
| **billing_cadence** | **String** |  |  |
| **status** | **String** |  |  |
| **current_period_start** | **Time** |  | [optional] |
| **current_period_end** | **Time** |  | [optional] |
| **cancel_at_period_end** | **Boolean** |  | [optional][default to false] |
| **cancel_effective_at** | **Time** |  | [optional] |
| **monthly_credits** | **Integer** |  | [optional][default to 0] |
| **pending_plan_code** | **String** |  | [optional] |
| **pending_plan_title** | **String** |  | [optional] |
| **pending_change_effective_at** | **Time** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::SubscriptionInfo.new(
  plan_code: null,
  plan_title: null,
  billing_cadence: null,
  status: null,
  current_period_start: null,
  current_period_end: null,
  cancel_at_period_end: null,
  cancel_effective_at: null,
  monthly_credits: null,
  pending_plan_code: null,
  pending_plan_title: null,
  pending_change_effective_at: null
)
```

