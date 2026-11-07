# ScrapeBadger::GitHubRepositoryFunding

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **github_sponsors** | [**Array&lt;GitHubRepositoryAccount&gt;**](GitHubRepositoryAccount.md) |  | [optional] |
| **links** | [**Array&lt;GitHubFundingLink&gt;**](GitHubFundingLink.md) |  | [optional] |
| **sponsorable_count** | **Integer** |  | [optional] |
| **sponsors_link** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubRepositoryFunding.new(
  github_sponsors: null,
  links: null,
  sponsorable_count: null,
  sponsors_link: null
)
```

