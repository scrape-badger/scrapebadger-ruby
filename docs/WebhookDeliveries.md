# ScrapeBadger::WebhookDeliveries

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **deliveries** | [**Array&lt;WebhookDelivery&gt;**](WebhookDelivery.md) |  |  |
| **window_hours** | **Integer** |  |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::WebhookDeliveries.new(
  deliveries: null,
  window_hours: 24
)
```

