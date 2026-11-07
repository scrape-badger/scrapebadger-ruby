# ScrapeBadger::GitHubActivityOverview

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **summary** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **repositories** | [**Array&lt;GitHubNamedLink&gt;**](GitHubNamedLink.md) |  | [optional] |
| **commits_percentage** | **Integer** |  | [optional] |
| **code_review_percentage** | **Integer** |  | [optional] |
| **pull_requests_percentage** | **Integer** |  | [optional] |
| **issues_percentage** | **Integer** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubActivityOverview.new(
  summary: null,
  description: null,
  repositories: null,
  commits_percentage: null,
  code_review_percentage: null,
  pull_requests_percentage: null,
  issues_percentage: null
)
```

