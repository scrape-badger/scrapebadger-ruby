# ScrapeBadger::AccountInfo

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **credits_balance** | **Integer** |  |  |
| **subscription_credits_balance** | **Integer** |  |  |
| **total_credits_balance** | **Integer** |  |  |
| **tier** | **String** |  |  |
| **rate_limit_per_minute** | **Integer** |  |  |
| **subscription** | [**SubscriptionInfo**](SubscriptionInfo.md) |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::AccountInfo.new(
  credits_balance: null,
  subscription_credits_balance: null,
  total_credits_balance: null,
  tier: null,
  rate_limit_per_minute: null,
  subscription: null
)
```

