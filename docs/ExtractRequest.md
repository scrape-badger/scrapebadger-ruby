# ScrapeBadger::ExtractRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | The page to fetch. |  |
| **wait_for** | **String** |  | [optional] |
| **country** | **String** |  | [optional] |
| **proxy_tier** | **String** | Proxy pool: simple, premium or ultra. | [optional][default to &#39;simple&#39;] |
| **extract_rules** | [**Hash&lt;String, ExtractRequestExtractRulesValue&gt;**](ExtractRequestExtractRulesValue.md) |  | [optional] |
| **ai_extract_rules** | **Hash&lt;String, String&gt;** |  | [optional] |
| **ai_query** | **String** |  | [optional] |
| **render_js** | **Boolean** | Render the page in a browser first. | [optional][default to false] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::ExtractRequest.new(
  url: null,
  wait_for: null,
  country: null,
  proxy_tier: null,
  extract_rules: null,
  ai_extract_rules: null,
  ai_query: null,
  render_js: null
)
```

