# ScrapeBadger::GitHubRepositoryReadme

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** |  |  |
| **html** | **String** |  |  |
| **link** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **path** | **String** |  | [optional] |
| **ref** | **String** |  | [optional] |
| **toc** | [**Array&lt;GitHubReadmeHeading&gt;**](GitHubReadmeHeading.md) |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubRepositoryReadme.new(
  text: null,
  html: null,
  link: null,
  name: null,
  path: null,
  ref: null,
  toc: null
)
```

