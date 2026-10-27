# ScrapeBadger::WebhookSecret

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **secret** | **String** |  |  |
| **signature_header** | **String** |  | [optional][default to &#39;X-ScrapeBadger-Signature&#39;] |
| **algorithm** | **String** |  | [optional][default to &#39;sha256&#x3D;&lt;hex HMAC-SHA256 of the raw request body&gt;&#39;] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::WebhookSecret.new(
  secret: null,
  signature_header: null,
  algorithm: null
)
```

