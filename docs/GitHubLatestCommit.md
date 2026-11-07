# ScrapeBadger::GitHubLatestCommit

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sha** | **String** |  |  |
| **link** | **String** |  |  |
| **message** | **String** |  |  |
| **message_html** | **String** |  | [optional] |
| **body** | **String** |  | [optional] |
| **body_html** | **String** |  | [optional] |
| **committed_at** | **String** |  | [optional] |
| **committed_utc** | **Float** |  | [optional] |
| **pushed_at** | **String** |  | [optional] |
| **pushed_utc** | **Float** |  | [optional] |
| **authors** | [**Array&lt;GitHubCommitActor&gt;**](GitHubCommitActor.md) |  | [optional] |
| **committer** | [**GitHubCommitActor**](GitHubCommitActor.md) |  | [optional] |
| **pusher** | [**GitHubCommitActor**](GitHubCommitActor.md) |  | [optional] |
| **checks** | [**GitHubCommitChecks**](GitHubCommitChecks.md) |  | [optional] |
| **is_spoofed** | **Boolean** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubLatestCommit.new(
  sha: null,
  link: null,
  message: null,
  message_html: null,
  body: null,
  body_html: null,
  committed_at: null,
  committed_utc: null,
  pushed_at: null,
  pushed_utc: null,
  authors: null,
  committer: null,
  pusher: null,
  checks: null,
  is_spoofed: null
)
```

