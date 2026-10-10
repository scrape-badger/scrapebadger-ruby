# ScrapeBadger::ScreenshotRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | The page to fetch. |  |
| **wait_for** | **String** |  | [optional] |
| **country** | **String** |  | [optional] |
| **proxy_tier** | **String** | Proxy pool: simple, premium or ultra. | [optional][default to &#39;simple&#39;] |
| **full_page** | **Boolean** | Capture the whole scrollable page instead of the viewport. | [optional][default to false] |
| **width** | **Integer** |  | [optional] |
| **height** | **Integer** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::ScreenshotRequest.new(
  url: null,
  wait_for: null,
  country: null,
  proxy_tier: null,
  full_page: null,
  width: null,
  height: null
)
```

