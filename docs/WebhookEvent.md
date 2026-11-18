# ScrapeBadger::WebhookEvent

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event** | **String** |  |  |
| **request_id** | **String** |  |  |
| **batch_id** | **String** |  |  |
| **status** | **Integer** | The call&#39;s own HTTP status. |  |
| **headers** | **Hash&lt;String, String&gt;** | The call&#39;s kept response headers, lower-case (content-type, x-credits-used, x-request-duration-ms, x-api-tier). |  |
| **result_url** | **String** |  |  |
| **result_expires_at** | **Integer** | Unix time. |  |
| **body_size** | **Integer** |  |  |
| **body** | **Object** |  |  |
| **body_omitted** | **Boolean** | Present (true) when the body was over 1 MB: fetch &#x60;result_url&#x60;. | [optional] |
| **attempt** | **Integer** |  |  |
| **sent_at** | **Integer** | Unix time of this attempt. |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::WebhookEvent.new(
  event: null,
  request_id: null,
  batch_id: null,
  status: null,
  headers: null,
  result_url: null,
  result_expires_at: null,
  body_size: null,
  body: null,
  body_omitted: null,
  attempt: null,
  sent_at: null
)
```

