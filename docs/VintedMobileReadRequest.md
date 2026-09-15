# ScrapeBadger::VintedMobileReadRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **market** | **String** | Vinted market code; uk aliases gb | [optional][default to &#39;fr&#39;] |
| **parameters** | **Hash&lt;String, Object&gt;** | Operation-specific parameters. GET /v1/vinted/mobile/operations lists types, required fields and examples. | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::VintedMobileReadRequest.new(
  market: null,
  parameters: null
)
```

