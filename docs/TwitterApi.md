# ScrapeBadger::TwitterApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**twitter_advanced_tweet_search**](TwitterApi.md#twitter_advanced_tweet_search) | **GET** /v1/twitter/tweets/advanced_search | Advanced tweet search |
| [**twitter_batch_get_users_by_ids**](TwitterApi.md#twitter_batch_get_users_by_ids) | **GET** /v1/twitter/users/batch_by_ids | Batch get users by IDs |
| [**twitter_batch_get_users_by_usernames**](TwitterApi.md#twitter_batch_get_users_by_usernames) | **GET** /v1/twitter/users/batch_by_usernames | Batch get users by usernames |
| [**twitter_configure_webhook_on_a_monitor**](TwitterApi.md#twitter_configure_webhook_on_a_monitor) | **POST** /v1/twitter/stream/webhooks | Configure webhook on a monitor |
| [**twitter_create_filter_rule**](TwitterApi.md#twitter_create_filter_rule) | **POST** /v1/twitter/stream/filter-rules | Create filter rule |
| [**twitter_create_stream_monitor**](TwitterApi.md#twitter_create_stream_monitor) | **POST** /v1/twitter/stream/monitors | Create stream monitor |
| [**twitter_delete_filter_rule**](TwitterApi.md#twitter_delete_filter_rule) | **DELETE** /v1/twitter/stream/filter-rules/{rule_id} | Delete filter rule |
| [**twitter_delete_stream_monitor**](TwitterApi.md#twitter_delete_stream_monitor) | **DELETE** /v1/twitter/stream/monitors/{monitor_id} | Delete stream monitor |
| [**twitter_get_article_by_id**](TwitterApi.md#twitter_get_article_by_id) | **GET** /v1/twitter/tweets/article/{article_id} | Get article by ID |
| [**twitter_get_broadcast_details**](TwitterApi.md#twitter_get_broadcast_details) | **GET** /v1/twitter/spaces/broadcast/{broadcast_id} | Get broadcast details |
| [**twitter_get_community_details**](TwitterApi.md#twitter_get_community_details) | **GET** /v1/twitter/communities/{community_id} | Get community details |
| [**twitter_get_community_notes**](TwitterApi.md#twitter_get_community_notes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/community_notes | Get community notes |
| [**twitter_get_community_tweets**](TwitterApi.md#twitter_get_community_tweets) | **GET** /v1/twitter/communities/{community_id}/tweets | Get community tweets |
| [**twitter_get_filter_rule**](TwitterApi.md#twitter_get_filter_rule) | **GET** /v1/twitter/stream/filter-rules/{rule_id} | Get filter rule |
| [**twitter_get_filter_rule_per_poll_rates**](TwitterApi.md#twitter_get_filter_rule_per_poll_rates) | **GET** /v1/twitter/stream/filter-rules-pricing | Get filter rule per-poll rates |
| [**twitter_get_list_details**](TwitterApi.md#twitter_get_list_details) | **GET** /v1/twitter/lists/{list_id}/detail | Get list details |
| [**twitter_get_list_tweets**](TwitterApi.md#twitter_get_list_tweets) | **GET** /v1/twitter/lists/{list_id}/tweets | Get list tweets |
| [**twitter_get_place_details**](TwitterApi.md#twitter_get_place_details) | **GET** /v1/twitter/geo/places/{place_id} | Get place details |
| [**twitter_get_similar_tweets**](TwitterApi.md#twitter_get_similar_tweets) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/similar | Get similar tweets |
| [**twitter_get_space_details**](TwitterApi.md#twitter_get_space_details) | **GET** /v1/twitter/spaces/{space_id} | Get Space details |
| [**twitter_get_stream_monitor**](TwitterApi.md#twitter_get_stream_monitor) | **GET** /v1/twitter/stream/monitors/{monitor_id} | Get stream monitor |
| [**twitter_get_trending_topics**](TwitterApi.md#twitter_get_trending_topics) | **GET** /v1/twitter/trends/ | Get trending topics |
| [**twitter_get_trends_by_location**](TwitterApi.md#twitter_get_trends_by_location) | **GET** /v1/twitter/trends/place/{woeid} | Get trends by location |
| [**twitter_get_tweet_details**](TwitterApi.md#twitter_get_tweet_details) | **GET** /v1/twitter/tweets/tweet/{tweet_id} | Get tweet details |
| [**twitter_get_tweet_edit_history**](TwitterApi.md#twitter_get_tweet_edit_history) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/edit_history | Get tweet edit history |
| [**twitter_get_tweet_favoriters**](TwitterApi.md#twitter_get_tweet_favoriters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/favoriters | Get tweet favoriters |
| [**twitter_get_tweet_quotes**](TwitterApi.md#twitter_get_tweet_quotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/quotes | Get tweet quotes |
| [**twitter_get_tweet_replies**](TwitterApi.md#twitter_get_tweet_replies) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/replies | Get tweet replies |
| [**twitter_get_tweet_retweeters**](TwitterApi.md#twitter_get_tweet_retweeters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/retweeters | Get tweet retweeters |
| [**twitter_get_tweets_by_ids**](TwitterApi.md#twitter_get_tweets_by_ids) | **GET** /v1/twitter/tweets/ | Get tweets by IDs |
| [**twitter_get_user_articles**](TwitterApi.md#twitter_get_user_articles) | **GET** /v1/twitter/users/{user_id}/articles | Get user articles |
| [**twitter_get_user_by_id**](TwitterApi.md#twitter_get_user_by_id) | **GET** /v1/twitter/users/{user_id}/by_id | Get user by ID |
| [**twitter_get_user_by_username**](TwitterApi.md#twitter_get_user_by_username) | **GET** /v1/twitter/users/{username}/by_username | Get user by username |
| [**twitter_get_user_followers**](TwitterApi.md#twitter_get_user_followers) | **GET** /v1/twitter/users/{username}/followers | Get user followers |
| [**twitter_get_user_following**](TwitterApi.md#twitter_get_user_following) | **GET** /v1/twitter/users/{username}/followings | Get user following |
| [**twitter_get_user_mentions**](TwitterApi.md#twitter_get_user_mentions) | **GET** /v1/twitter/users/{username}/mentions | Get user mentions |
| [**twitter_get_user_subscriptions**](TwitterApi.md#twitter_get_user_subscriptions) | **GET** /v1/twitter/users/{user_id}/subscriptions | Get user subscriptions |
| [**twitter_get_user_tweets**](TwitterApi.md#twitter_get_user_tweets) | **GET** /v1/twitter/users/{username}/latest_tweets | Get user tweets |
| [**twitter_list_billing_logs**](TwitterApi.md#twitter_list_billing_logs) | **GET** /v1/twitter/stream/billing-logs | List billing logs |
| [**twitter_list_delivery_logs_for_a_filter_rule**](TwitterApi.md#twitter_list_delivery_logs_for_a_filter_rule) | **GET** /v1/twitter/stream/filter-rules/{rule_id}/logs | List delivery logs for a filter rule |
| [**twitter_list_filter_rules**](TwitterApi.md#twitter_list_filter_rules) | **GET** /v1/twitter/stream/filter-rules | List filter rules |
| [**twitter_list_stream_monitors**](TwitterApi.md#twitter_list_stream_monitors) | **GET** /v1/twitter/stream/monitors | List stream monitors |
| [**twitter_list_tweet_delivery_logs**](TwitterApi.md#twitter_list_tweet_delivery_logs) | **GET** /v1/twitter/stream/logs | List tweet delivery logs |
| [**twitter_list_webhooks**](TwitterApi.md#twitter_list_webhooks) | **GET** /v1/twitter/stream/webhooks | List webhooks |
| [**twitter_remove_webhook_from_monitor**](TwitterApi.md#twitter_remove_webhook_from_monitor) | **DELETE** /v1/twitter/stream/webhooks/{webhook_id} | Remove webhook from monitor |
| [**twitter_search_communities**](TwitterApi.md#twitter_search_communities) | **GET** /v1/twitter/communities/search | Search communities |
| [**twitter_search_list_tweets**](TwitterApi.md#twitter_search_list_tweets) | **GET** /v1/twitter/lists/{list_id}/search_tweets | Search list tweets |
| [**twitter_search_places**](TwitterApi.md#twitter_search_places) | **GET** /v1/twitter/geo/search | Search places |
| [**twitter_search_users**](TwitterApi.md#twitter_search_users) | **GET** /v1/twitter/users/search_users | Search users |
| [**twitter_test_webhook_delivery**](TwitterApi.md#twitter_test_webhook_delivery) | **POST** /v1/twitter/stream/webhooks/test | Test webhook delivery |
| [**twitter_twitter_scraper_health_check**](TwitterApi.md#twitter_twitter_scraper_health_check) | **GET** /v1/twitter/health | Twitter scraper health check |
| [**twitter_twitter_scraper_health_check_head**](TwitterApi.md#twitter_twitter_scraper_health_check_head) | **HEAD** /v1/twitter/health | Twitter scraper health check |
| [**twitter_update_filter_rule**](TwitterApi.md#twitter_update_filter_rule) | **PATCH** /v1/twitter/stream/filter-rules/{rule_id} | Update filter rule |
| [**twitter_update_stream_monitor**](TwitterApi.md#twitter_update_stream_monitor) | **PATCH** /v1/twitter/stream/monitors/{monitor_id} | Update stream monitor |
| [**twitter_validate_search_query**](TwitterApi.md#twitter_validate_search_query) | **POST** /v1/twitter/stream/filter-rules/validate | Validate search query |


## twitter_advanced_tweet_search

> Object twitter_advanced_tweet_search(query, opts)

Advanced tweet search

Search tweets with advanced options.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
query = 'query_example' # String | 
opts = {
  query_type: 'query_type_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # Advanced tweet search
  result = api_instance.twitter_advanced_tweet_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_advanced_tweet_search: #{e}"
end
```

#### Using the twitter_advanced_tweet_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_advanced_tweet_search_with_http_info(query, opts)

```ruby
begin
  # Advanced tweet search
  data, status_code, headers = api_instance.twitter_advanced_tweet_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_advanced_tweet_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **query_type** | **String** |  | [optional] |
| **count** | **Integer** |  | [optional] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_batch_get_users_by_ids

> Object twitter_batch_get_users_by_ids(user_ids)

Batch get users by IDs

Get multiple user profiles by their numeric IDs (comma-separated).

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
user_ids = 'user_ids_example' # String | 

begin
  # Batch get users by IDs
  result = api_instance.twitter_batch_get_users_by_ids(user_ids)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_batch_get_users_by_ids: #{e}"
end
```

#### Using the twitter_batch_get_users_by_ids_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_batch_get_users_by_ids_with_http_info(user_ids)

```ruby
begin
  # Batch get users by IDs
  data, status_code, headers = api_instance.twitter_batch_get_users_by_ids_with_http_info(user_ids)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_batch_get_users_by_ids_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_ids** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_batch_get_users_by_usernames

> Object twitter_batch_get_users_by_usernames(usernames)

Batch get users by usernames

Get multiple user profiles by their usernames (comma-separated).

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
usernames = 'usernames_example' # String | 

begin
  # Batch get users by usernames
  result = api_instance.twitter_batch_get_users_by_usernames(usernames)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_batch_get_users_by_usernames: #{e}"
end
```

#### Using the twitter_batch_get_users_by_usernames_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_batch_get_users_by_usernames_with_http_info(usernames)

```ruby
begin
  # Batch get users by usernames
  data, status_code, headers = api_instance.twitter_batch_get_users_by_usernames_with_http_info(usernames)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_batch_get_users_by_usernames_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **usernames** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_configure_webhook_on_a_monitor

> <WebhookResponse> twitter_configure_webhook_on_a_monitor(webhook_create)

Configure webhook on a monitor

Configure a webhook delivery URL on a stream monitor.  The secret is returned only once on creation. Subsequent calls show secret_set: bool. If monitor already has a webhook, delete it first (409 is returned).

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
webhook_create = ScrapeBadger::WebhookCreate.new({monitor_id: 'monitor_id_example', url: 'url_example'}) # WebhookCreate | 

begin
  # Configure webhook on a monitor
  result = api_instance.twitter_configure_webhook_on_a_monitor(webhook_create)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_configure_webhook_on_a_monitor: #{e}"
end
```

#### Using the twitter_configure_webhook_on_a_monitor_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookResponse>, Integer, Hash)> twitter_configure_webhook_on_a_monitor_with_http_info(webhook_create)

```ruby
begin
  # Configure webhook on a monitor
  data, status_code, headers = api_instance.twitter_configure_webhook_on_a_monitor_with_http_info(webhook_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_configure_webhook_on_a_monitor_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_create** | [**WebhookCreate**](WebhookCreate.md) |  |  |

### Return type

[**WebhookResponse**](WebhookResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## twitter_create_filter_rule

> <FilterRuleResponse> twitter_create_filter_rule(filter_rule_create)

Create filter rule

Create a new query-based tweet filter rule.  The rule starts in 'active' status immediately. Credits must be positive. The (api_key_id, tag) pair must be unique.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
filter_rule_create = ScrapeBadger::FilterRuleCreate.new({tag: 'tag_example', query: 'query_example', interval_seconds: 3.56}) # FilterRuleCreate | 

begin
  # Create filter rule
  result = api_instance.twitter_create_filter_rule(filter_rule_create)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_create_filter_rule: #{e}"
end
```

#### Using the twitter_create_filter_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FilterRuleResponse>, Integer, Hash)> twitter_create_filter_rule_with_http_info(filter_rule_create)

```ruby
begin
  # Create filter rule
  data, status_code, headers = api_instance.twitter_create_filter_rule_with_http_info(filter_rule_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FilterRuleResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_create_filter_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **filter_rule_create** | [**FilterRuleCreate**](FilterRuleCreate.md) |  |  |

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## twitter_create_stream_monitor

> <StreamMonitorResponse> twitter_create_stream_monitor(stream_monitor_create)

Create stream monitor

Create a new stream monitor to watch Twitter accounts in real-time.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
stream_monitor_create = ScrapeBadger::StreamMonitorCreate.new({name: 'name_example', usernames: ['usernames_example']}) # StreamMonitorCreate | 

begin
  # Create stream monitor
  result = api_instance.twitter_create_stream_monitor(stream_monitor_create)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_create_stream_monitor: #{e}"
end
```

#### Using the twitter_create_stream_monitor_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StreamMonitorResponse>, Integer, Hash)> twitter_create_stream_monitor_with_http_info(stream_monitor_create)

```ruby
begin
  # Create stream monitor
  data, status_code, headers = api_instance.twitter_create_stream_monitor_with_http_info(stream_monitor_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StreamMonitorResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_create_stream_monitor_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **stream_monitor_create** | [**StreamMonitorCreate**](StreamMonitorCreate.md) |  |  |

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## twitter_delete_filter_rule

> twitter_delete_filter_rule(rule_id)

Delete filter rule

Delete a filter rule and all its logs.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
rule_id = 'rule_id_example' # String | 

begin
  # Delete filter rule
  api_instance.twitter_delete_filter_rule(rule_id)
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_delete_filter_rule: #{e}"
end
```

#### Using the twitter_delete_filter_rule_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> twitter_delete_filter_rule_with_http_info(rule_id)

```ruby
begin
  # Delete filter rule
  data, status_code, headers = api_instance.twitter_delete_filter_rule_with_http_info(rule_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_delete_filter_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rule_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_delete_stream_monitor

> twitter_delete_stream_monitor(monitor_id)

Delete stream monitor

Delete a stream monitor and all its logs.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
monitor_id = 'monitor_id_example' # String | 

begin
  # Delete stream monitor
  api_instance.twitter_delete_stream_monitor(monitor_id)
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_delete_stream_monitor: #{e}"
end
```

#### Using the twitter_delete_stream_monitor_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> twitter_delete_stream_monitor_with_http_info(monitor_id)

```ruby
begin
  # Delete stream monitor
  data, status_code, headers = api_instance.twitter_delete_stream_monitor_with_http_info(monitor_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_delete_stream_monitor_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monitor_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_article_by_id

> Object twitter_get_article_by_id(article_id)

Get article by ID

Get a long-form article by its ID.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
article_id = 'article_id_example' # String | 

begin
  # Get article by ID
  result = api_instance.twitter_get_article_by_id(article_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_article_by_id: #{e}"
end
```

#### Using the twitter_get_article_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_article_by_id_with_http_info(article_id)

```ruby
begin
  # Get article by ID
  data, status_code, headers = api_instance.twitter_get_article_by_id_with_http_info(article_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_article_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **article_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_broadcast_details

> Object twitter_get_broadcast_details(broadcast_id)

Get broadcast details

Get details of a live video broadcast.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
broadcast_id = 'broadcast_id_example' # String | 

begin
  # Get broadcast details
  result = api_instance.twitter_get_broadcast_details(broadcast_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_broadcast_details: #{e}"
end
```

#### Using the twitter_get_broadcast_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_broadcast_details_with_http_info(broadcast_id)

```ruby
begin
  # Get broadcast details
  data, status_code, headers = api_instance.twitter_get_broadcast_details_with_http_info(broadcast_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_broadcast_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **broadcast_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_community_details

> Object twitter_get_community_details(community_id)

Get community details

Get details of a specific community.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
community_id = 'community_id_example' # String | 

begin
  # Get community details
  result = api_instance.twitter_get_community_details(community_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_community_details: #{e}"
end
```

#### Using the twitter_get_community_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_community_details_with_http_info(community_id)

```ruby
begin
  # Get community details
  data, status_code, headers = api_instance.twitter_get_community_details_with_http_info(community_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_community_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **community_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_community_notes

> Object twitter_get_community_notes(tweet_id)

Get community notes

Get community notes (Birdwatch) for a specific tweet.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
tweet_id = 'tweet_id_example' # String | 

begin
  # Get community notes
  result = api_instance.twitter_get_community_notes(tweet_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_community_notes: #{e}"
end
```

#### Using the twitter_get_community_notes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_community_notes_with_http_info(tweet_id)

```ruby
begin
  # Get community notes
  data, status_code, headers = api_instance.twitter_get_community_notes_with_http_info(tweet_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_community_notes_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tweet_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_community_tweets

> Object twitter_get_community_tweets(community_id, opts)

Get community tweets

Get tweets from a specific community.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
community_id = 'community_id_example' # String | 
opts = {
  tweet_type: 'tweet_type_example', # String | 
  cursor: 'cursor_example' # String | 
}

begin
  # Get community tweets
  result = api_instance.twitter_get_community_tweets(community_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_community_tweets: #{e}"
end
```

#### Using the twitter_get_community_tweets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_community_tweets_with_http_info(community_id, opts)

```ruby
begin
  # Get community tweets
  data, status_code, headers = api_instance.twitter_get_community_tweets_with_http_info(community_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_community_tweets_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **community_id** | **String** |  |  |
| **tweet_type** | **String** |  | [optional] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_filter_rule

> <FilterRuleResponse> twitter_get_filter_rule(rule_id)

Get filter rule

Get a single filter rule by ID.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
rule_id = 'rule_id_example' # String | 

begin
  # Get filter rule
  result = api_instance.twitter_get_filter_rule(rule_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_filter_rule: #{e}"
end
```

#### Using the twitter_get_filter_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FilterRuleResponse>, Integer, Hash)> twitter_get_filter_rule_with_http_info(rule_id)

```ruby
begin
  # Get filter rule
  data, status_code, headers = api_instance.twitter_get_filter_rule_with_http_info(rule_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FilterRuleResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_filter_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rule_id** | **String** |  |  |

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_filter_rule_per_poll_rates

> <PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse> twitter_get_filter_rule_per_poll_rates

Get filter rule per-poll rates

Current per-poll rates (auth required — used by SDK + dashboard).

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new

begin
  # Get filter rule per-poll rates
  result = api_instance.twitter_get_filter_rule_per_poll_rates
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_filter_rule_per_poll_rates: #{e}"
end
```

#### Using the twitter_get_filter_rule_per_poll_rates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse>, Integer, Hash)> twitter_get_filter_rule_per_poll_rates_with_http_info

```ruby
begin
  # Get filter rule per-poll rates
  data, status_code, headers = api_instance.twitter_get_filter_rule_per_poll_rates_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_filter_rule_per_poll_rates_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse**](PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_list_details

> Object twitter_get_list_details(list_id)

Get list details

Get details of a specific list.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
list_id = 'list_id_example' # String | 

begin
  # Get list details
  result = api_instance.twitter_get_list_details(list_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_list_details: #{e}"
end
```

#### Using the twitter_get_list_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_list_details_with_http_info(list_id)

```ruby
begin
  # Get list details
  data, status_code, headers = api_instance.twitter_get_list_details_with_http_info(list_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_list_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_list_tweets

> Object twitter_get_list_tweets(list_id, opts)

Get list tweets

Get tweets from a specific list.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
list_id = 'list_id_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get list tweets
  result = api_instance.twitter_get_list_tweets(list_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_list_tweets: #{e}"
end
```

#### Using the twitter_get_list_tweets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_list_tweets_with_http_info(list_id, opts)

```ruby
begin
  # Get list tweets
  data, status_code, headers = api_instance.twitter_get_list_tweets_with_http_info(list_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_list_tweets_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list_id** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_place_details

> Object twitter_get_place_details(place_id)

Get place details

Get details of a specific place.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
place_id = 'place_id_example' # String | 

begin
  # Get place details
  result = api_instance.twitter_get_place_details(place_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_place_details: #{e}"
end
```

#### Using the twitter_get_place_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_place_details_with_http_info(place_id)

```ruby
begin
  # Get place details
  data, status_code, headers = api_instance.twitter_get_place_details_with_http_info(place_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_place_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **place_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_similar_tweets

> Object twitter_get_similar_tweets(tweet_id)

Get similar tweets

Get tweets similar to a specific tweet.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
tweet_id = 'tweet_id_example' # String | 

begin
  # Get similar tweets
  result = api_instance.twitter_get_similar_tweets(tweet_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_similar_tweets: #{e}"
end
```

#### Using the twitter_get_similar_tweets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_similar_tweets_with_http_info(tweet_id)

```ruby
begin
  # Get similar tweets
  data, status_code, headers = api_instance.twitter_get_similar_tweets_with_http_info(tweet_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_similar_tweets_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tweet_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_space_details

> Object twitter_get_space_details(space_id)

Get Space details

Get details of a Twitter Space.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
space_id = 'space_id_example' # String | 

begin
  # Get Space details
  result = api_instance.twitter_get_space_details(space_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_space_details: #{e}"
end
```

#### Using the twitter_get_space_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_space_details_with_http_info(space_id)

```ruby
begin
  # Get Space details
  data, status_code, headers = api_instance.twitter_get_space_details_with_http_info(space_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_space_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **space_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_stream_monitor

> <StreamMonitorResponse> twitter_get_stream_monitor(monitor_id)

Get stream monitor

Get a single stream monitor by ID.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
monitor_id = 'monitor_id_example' # String | 

begin
  # Get stream monitor
  result = api_instance.twitter_get_stream_monitor(monitor_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_stream_monitor: #{e}"
end
```

#### Using the twitter_get_stream_monitor_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StreamMonitorResponse>, Integer, Hash)> twitter_get_stream_monitor_with_http_info(monitor_id)

```ruby
begin
  # Get stream monitor
  data, status_code, headers = api_instance.twitter_get_stream_monitor_with_http_info(monitor_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StreamMonitorResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_stream_monitor_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monitor_id** | **String** |  |  |

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_trending_topics

> Object twitter_get_trending_topics(opts)

Get trending topics

Get trending topics.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
opts = {
  category: 'category_example', # String | 
  count: 56 # Integer | 
}

begin
  # Get trending topics
  result = api_instance.twitter_get_trending_topics(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_trending_topics: #{e}"
end
```

#### Using the twitter_get_trending_topics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_trending_topics_with_http_info(opts)

```ruby
begin
  # Get trending topics
  data, status_code, headers = api_instance.twitter_get_trending_topics_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_trending_topics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category** | **String** |  | [optional] |
| **count** | **Integer** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_trends_by_location

> Object twitter_get_trends_by_location(woeid)

Get trends by location

Get trending topics for a specific location (WOEID).

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
woeid = 'woeid_example' # String | 

begin
  # Get trends by location
  result = api_instance.twitter_get_trends_by_location(woeid)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_trends_by_location: #{e}"
end
```

#### Using the twitter_get_trends_by_location_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_trends_by_location_with_http_info(woeid)

```ruby
begin
  # Get trends by location
  data, status_code, headers = api_instance.twitter_get_trends_by_location_with_http_info(woeid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_trends_by_location_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **woeid** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_tweet_details

> Object twitter_get_tweet_details(tweet_id, opts)

Get tweet details

Get detailed information about a specific tweet.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
tweet_id = 'tweet_id_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get tweet details
  result = api_instance.twitter_get_tweet_details(tweet_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_details: #{e}"
end
```

#### Using the twitter_get_tweet_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_tweet_details_with_http_info(tweet_id, opts)

```ruby
begin
  # Get tweet details
  data, status_code, headers = api_instance.twitter_get_tweet_details_with_http_info(tweet_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tweet_id** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_tweet_edit_history

> Object twitter_get_tweet_edit_history(tweet_id)

Get tweet edit history

Get the edit history of a tweet.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
tweet_id = 'tweet_id_example' # String | 

begin
  # Get tweet edit history
  result = api_instance.twitter_get_tweet_edit_history(tweet_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_edit_history: #{e}"
end
```

#### Using the twitter_get_tweet_edit_history_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_tweet_edit_history_with_http_info(tweet_id)

```ruby
begin
  # Get tweet edit history
  data, status_code, headers = api_instance.twitter_get_tweet_edit_history_with_http_info(tweet_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_edit_history_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tweet_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_tweet_favoriters

> Object twitter_get_tweet_favoriters(tweet_id, opts)

Get tweet favoriters

Get users who favorited a specific tweet.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
tweet_id = 'tweet_id_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get tweet favoriters
  result = api_instance.twitter_get_tweet_favoriters(tweet_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_favoriters: #{e}"
end
```

#### Using the twitter_get_tweet_favoriters_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_tweet_favoriters_with_http_info(tweet_id, opts)

```ruby
begin
  # Get tweet favoriters
  data, status_code, headers = api_instance.twitter_get_tweet_favoriters_with_http_info(tweet_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_favoriters_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tweet_id** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_tweet_quotes

> Object twitter_get_tweet_quotes(tweet_id, opts)

Get tweet quotes

Get tweets that quote a specific tweet.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
tweet_id = 'tweet_id_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get tweet quotes
  result = api_instance.twitter_get_tweet_quotes(tweet_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_quotes: #{e}"
end
```

#### Using the twitter_get_tweet_quotes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_tweet_quotes_with_http_info(tweet_id, opts)

```ruby
begin
  # Get tweet quotes
  data, status_code, headers = api_instance.twitter_get_tweet_quotes_with_http_info(tweet_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_quotes_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tweet_id** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_tweet_replies

> Object twitter_get_tweet_replies(tweet_id, opts)

Get tweet replies

Get replies to a specific tweet.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
tweet_id = 'tweet_id_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get tweet replies
  result = api_instance.twitter_get_tweet_replies(tweet_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_replies: #{e}"
end
```

#### Using the twitter_get_tweet_replies_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_tweet_replies_with_http_info(tweet_id, opts)

```ruby
begin
  # Get tweet replies
  data, status_code, headers = api_instance.twitter_get_tweet_replies_with_http_info(tweet_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_replies_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tweet_id** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_tweet_retweeters

> Object twitter_get_tweet_retweeters(tweet_id, opts)

Get tweet retweeters

Get users who retweeted a specific tweet.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
tweet_id = 'tweet_id_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get tweet retweeters
  result = api_instance.twitter_get_tweet_retweeters(tweet_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_retweeters: #{e}"
end
```

#### Using the twitter_get_tweet_retweeters_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_tweet_retweeters_with_http_info(tweet_id, opts)

```ruby
begin
  # Get tweet retweeters
  data, status_code, headers = api_instance.twitter_get_tweet_retweeters_with_http_info(tweet_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweet_retweeters_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tweet_id** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_tweets_by_ids

> Object twitter_get_tweets_by_ids(tweets)

Get tweets by IDs

Get multiple tweets by their IDs.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
tweets = 'tweets_example' # String | 

begin
  # Get tweets by IDs
  result = api_instance.twitter_get_tweets_by_ids(tweets)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweets_by_ids: #{e}"
end
```

#### Using the twitter_get_tweets_by_ids_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_tweets_by_ids_with_http_info(tweets)

```ruby
begin
  # Get tweets by IDs
  data, status_code, headers = api_instance.twitter_get_tweets_by_ids_with_http_info(tweets)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_tweets_by_ids_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tweets** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_user_articles

> Object twitter_get_user_articles(user_id, opts)

Get user articles

Get long-form articles written by a user.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
user_id = 'user_id_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get user articles
  result = api_instance.twitter_get_user_articles(user_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_articles: #{e}"
end
```

#### Using the twitter_get_user_articles_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_user_articles_with_http_info(user_id, opts)

```ruby
begin
  # Get user articles
  data, status_code, headers = api_instance.twitter_get_user_articles_with_http_info(user_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_articles_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_user_by_id

> Object twitter_get_user_by_id(user_id)

Get user by ID

Get user profile by user ID.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
user_id = 'user_id_example' # String | 

begin
  # Get user by ID
  result = api_instance.twitter_get_user_by_id(user_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_by_id: #{e}"
end
```

#### Using the twitter_get_user_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_user_by_id_with_http_info(user_id)

```ruby
begin
  # Get user by ID
  data, status_code, headers = api_instance.twitter_get_user_by_id_with_http_info(user_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_user_by_username

> Object twitter_get_user_by_username(username)

Get user by username

Get user profile by username.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
username = 'username_example' # String | 

begin
  # Get user by username
  result = api_instance.twitter_get_user_by_username(username)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_by_username: #{e}"
end
```

#### Using the twitter_get_user_by_username_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_user_by_username_with_http_info(username)

```ruby
begin
  # Get user by username
  data, status_code, headers = api_instance.twitter_get_user_by_username_with_http_info(username)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_by_username_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_user_followers

> Object twitter_get_user_followers(username, opts)

Get user followers

Get followers of a specific user.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
username = 'username_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get user followers
  result = api_instance.twitter_get_user_followers(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_followers: #{e}"
end
```

#### Using the twitter_get_user_followers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_user_followers_with_http_info(username, opts)

```ruby
begin
  # Get user followers
  data, status_code, headers = api_instance.twitter_get_user_followers_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_followers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_user_following

> Object twitter_get_user_following(username, opts)

Get user following

Get users that a specific user is following.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
username = 'username_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get user following
  result = api_instance.twitter_get_user_following(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_following: #{e}"
end
```

#### Using the twitter_get_user_following_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_user_following_with_http_info(username, opts)

```ruby
begin
  # Get user following
  data, status_code, headers = api_instance.twitter_get_user_following_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_following_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_user_mentions

> Object twitter_get_user_mentions(username, opts)

Get user mentions

Get tweets mentioning a specific user.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
username = 'username_example' # String | 
opts = {
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # Get user mentions
  result = api_instance.twitter_get_user_mentions(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_mentions: #{e}"
end
```

#### Using the twitter_get_user_mentions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_user_mentions_with_http_info(username, opts)

```ruby
begin
  # Get user mentions
  data, status_code, headers = api_instance.twitter_get_user_mentions_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_mentions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **count** | **Integer** |  | [optional] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_user_subscriptions

> Object twitter_get_user_subscriptions(user_id, opts)

Get user subscriptions

Get subscriptions of a specific user.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
user_id = 'user_id_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get user subscriptions
  result = api_instance.twitter_get_user_subscriptions(user_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_subscriptions: #{e}"
end
```

#### Using the twitter_get_user_subscriptions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_user_subscriptions_with_http_info(user_id, opts)

```ruby
begin
  # Get user subscriptions
  data, status_code, headers = api_instance.twitter_get_user_subscriptions_with_http_info(user_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_subscriptions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_get_user_tweets

> Object twitter_get_user_tweets(username, opts)

Get user tweets

Get latest tweets from a specific user.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
username = 'username_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Get user tweets
  result = api_instance.twitter_get_user_tweets(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_tweets: #{e}"
end
```

#### Using the twitter_get_user_tweets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_get_user_tweets_with_http_info(username, opts)

```ruby
begin
  # Get user tweets
  data, status_code, headers = api_instance.twitter_get_user_tweets_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_get_user_tweets_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_list_billing_logs

> <BillingLogListResponse> twitter_list_billing_logs(opts)

List billing logs

List billing activity logs for the authenticated API key's monitors.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
opts = {
  monitor_id: 'monitor_id_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # List billing logs
  result = api_instance.twitter_list_billing_logs(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_billing_logs: #{e}"
end
```

#### Using the twitter_list_billing_logs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BillingLogListResponse>, Integer, Hash)> twitter_list_billing_logs_with_http_info(opts)

```ruby
begin
  # List billing logs
  data, status_code, headers = api_instance.twitter_list_billing_logs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BillingLogListResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_billing_logs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monitor_id** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 20] |

### Return type

[**BillingLogListResponse**](BillingLogListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_list_delivery_logs_for_a_filter_rule

> <FilterRuleDeliveryLogListResponse> twitter_list_delivery_logs_for_a_filter_rule(rule_id, opts)

List delivery logs for a filter rule

List tweet delivery logs for a specific filter rule.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
rule_id = 'rule_id_example' # String | 
opts = {
  delivery_status: 'delivery_status_example', # String | 
  author_username: 'author_username_example', # String | 
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  sort: 'asc' # String | 
}

begin
  # List delivery logs for a filter rule
  result = api_instance.twitter_list_delivery_logs_for_a_filter_rule(rule_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_delivery_logs_for_a_filter_rule: #{e}"
end
```

#### Using the twitter_list_delivery_logs_for_a_filter_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FilterRuleDeliveryLogListResponse>, Integer, Hash)> twitter_list_delivery_logs_for_a_filter_rule_with_http_info(rule_id, opts)

```ruby
begin
  # List delivery logs for a filter rule
  data, status_code, headers = api_instance.twitter_list_delivery_logs_for_a_filter_rule_with_http_info(rule_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FilterRuleDeliveryLogListResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_delivery_logs_for_a_filter_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rule_id** | **String** |  |  |
| **delivery_status** | **String** |  | [optional] |
| **author_username** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 20] |
| **sort** | **String** |  | [optional][default to &#39;desc&#39;] |

### Return type

[**FilterRuleDeliveryLogListResponse**](FilterRuleDeliveryLogListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_list_filter_rules

> <FilterRuleListResponse> twitter_list_filter_rules(opts)

List filter rules

List all filter rules for the authenticated API key.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
opts = {
  status: 'status_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # List filter rules
  result = api_instance.twitter_list_filter_rules(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_filter_rules: #{e}"
end
```

#### Using the twitter_list_filter_rules_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FilterRuleListResponse>, Integer, Hash)> twitter_list_filter_rules_with_http_info(opts)

```ruby
begin
  # List filter rules
  data, status_code, headers = api_instance.twitter_list_filter_rules_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FilterRuleListResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_filter_rules_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 20] |

### Return type

[**FilterRuleListResponse**](FilterRuleListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_list_stream_monitors

> <StreamMonitorListResponse> twitter_list_stream_monitors(opts)

List stream monitors

List all stream monitors for the authenticated API key.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
opts = {
  status: 'status_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # List stream monitors
  result = api_instance.twitter_list_stream_monitors(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_stream_monitors: #{e}"
end
```

#### Using the twitter_list_stream_monitors_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StreamMonitorListResponse>, Integer, Hash)> twitter_list_stream_monitors_with_http_info(opts)

```ruby
begin
  # List stream monitors
  data, status_code, headers = api_instance.twitter_list_stream_monitors_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StreamMonitorListResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_stream_monitors_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 20] |

### Return type

[**StreamMonitorListResponse**](StreamMonitorListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_list_tweet_delivery_logs

> <TweetDeliveryLogListResponse> twitter_list_tweet_delivery_logs(opts)

List tweet delivery logs

List tweet delivery logs for the authenticated API key's monitors.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
opts = {
  monitor_id: 'monitor_id_example', # String | 
  author_username: 'author_username_example', # String | 
  delivery_status: 'delivery_status_example', # String | 
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  sort: 'asc' # String | 
}

begin
  # List tweet delivery logs
  result = api_instance.twitter_list_tweet_delivery_logs(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_tweet_delivery_logs: #{e}"
end
```

#### Using the twitter_list_tweet_delivery_logs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TweetDeliveryLogListResponse>, Integer, Hash)> twitter_list_tweet_delivery_logs_with_http_info(opts)

```ruby
begin
  # List tweet delivery logs
  data, status_code, headers = api_instance.twitter_list_tweet_delivery_logs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TweetDeliveryLogListResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_tweet_delivery_logs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monitor_id** | **String** |  | [optional] |
| **author_username** | **String** |  | [optional] |
| **delivery_status** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |
| **page_size** | **Integer** |  | [optional][default to 20] |
| **sort** | **String** |  | [optional][default to &#39;desc&#39;] |

### Return type

[**TweetDeliveryLogListResponse**](TweetDeliveryLogListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_list_webhooks

> <WebhookListResponse> twitter_list_webhooks(opts)

List webhooks

List all webhook-configured monitors for the authenticated API key.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
opts = {
  monitor_id: 'monitor_id_example' # String | 
}

begin
  # List webhooks
  result = api_instance.twitter_list_webhooks(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_webhooks: #{e}"
end
```

#### Using the twitter_list_webhooks_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookListResponse>, Integer, Hash)> twitter_list_webhooks_with_http_info(opts)

```ruby
begin
  # List webhooks
  data, status_code, headers = api_instance.twitter_list_webhooks_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookListResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_list_webhooks_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monitor_id** | **String** |  | [optional] |

### Return type

[**WebhookListResponse**](WebhookListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_remove_webhook_from_monitor

> twitter_remove_webhook_from_monitor(webhook_id)

Remove webhook from monitor

Remove webhook configuration from a monitor. webhook_id is the monitor_id.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
webhook_id = 'webhook_id_example' # String | 

begin
  # Remove webhook from monitor
  api_instance.twitter_remove_webhook_from_monitor(webhook_id)
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_remove_webhook_from_monitor: #{e}"
end
```

#### Using the twitter_remove_webhook_from_monitor_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> twitter_remove_webhook_from_monitor_with_http_info(webhook_id)

```ruby
begin
  # Remove webhook from monitor
  data, status_code, headers = api_instance.twitter_remove_webhook_from_monitor_with_http_info(webhook_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_remove_webhook_from_monitor_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_search_communities

> Object twitter_search_communities(query, opts)

Search communities

Search for communities by query.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
query = 'query_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Search communities
  result = api_instance.twitter_search_communities(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_search_communities: #{e}"
end
```

#### Using the twitter_search_communities_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_search_communities_with_http_info(query, opts)

```ruby
begin
  # Search communities
  data, status_code, headers = api_instance.twitter_search_communities_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_search_communities_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_search_list_tweets

> Object twitter_search_list_tweets(list_id, query, opts)

Search list tweets

Search tweets within a specific list.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
list_id = 'list_id_example' # String | 
query = 'query_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Search list tweets
  result = api_instance.twitter_search_list_tweets(list_id, query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_search_list_tweets: #{e}"
end
```

#### Using the twitter_search_list_tweets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_search_list_tweets_with_http_info(list_id, query, opts)

```ruby
begin
  # Search list tweets
  data, status_code, headers = api_instance.twitter_search_list_tweets_with_http_info(list_id, query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_search_list_tweets_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list_id** | **String** |  |  |
| **query** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_search_places

> Object twitter_search_places(opts)

Search places

Search for places by query or coordinates.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
opts = {
  query: 'query_example', # String | 
  lat: 8.14, # Float | 
  long: 8.14 # Float | 
}

begin
  # Search places
  result = api_instance.twitter_search_places(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_search_places: #{e}"
end
```

#### Using the twitter_search_places_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_search_places_with_http_info(opts)

```ruby
begin
  # Search places
  data, status_code, headers = api_instance.twitter_search_places_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_search_places_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  | [optional] |
| **lat** | **Float** |  | [optional] |
| **long** | **Float** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_search_users

> Object twitter_search_users(query, opts)

Search users

Search for users by query.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
query = 'query_example' # String | 
opts = {
  cursor: 'cursor_example' # String | 
}

begin
  # Search users
  result = api_instance.twitter_search_users(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_search_users: #{e}"
end
```

#### Using the twitter_search_users_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_search_users_with_http_info(query, opts)

```ruby
begin
  # Search users
  data, status_code, headers = api_instance.twitter_search_users_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_search_users_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_test_webhook_delivery

> <WebhookTestResponse> twitter_test_webhook_delivery(webhook_test_request)

Test webhook delivery

Send a test payload to a monitor's webhook URL.  The test payload has type=\"test\" instead of type=\"tweet\". Makes a synchronous HTTP POST and returns the delivery result.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
webhook_test_request = ScrapeBadger::WebhookTestRequest.new({monitor_id: 'monitor_id_example'}) # WebhookTestRequest | 

begin
  # Test webhook delivery
  result = api_instance.twitter_test_webhook_delivery(webhook_test_request)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_test_webhook_delivery: #{e}"
end
```

#### Using the twitter_test_webhook_delivery_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookTestResponse>, Integer, Hash)> twitter_test_webhook_delivery_with_http_info(webhook_test_request)

```ruby
begin
  # Test webhook delivery
  data, status_code, headers = api_instance.twitter_test_webhook_delivery_with_http_info(webhook_test_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookTestResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_test_webhook_delivery_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_test_request** | [**WebhookTestRequest**](WebhookTestRequest.md) |  |  |

### Return type

[**WebhookTestResponse**](WebhookTestResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## twitter_twitter_scraper_health_check

> Object twitter_twitter_scraper_health_check

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new

begin
  # Twitter scraper health check
  result = api_instance.twitter_twitter_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_twitter_scraper_health_check: #{e}"
end
```

#### Using the twitter_twitter_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_twitter_scraper_health_check_with_http_info

```ruby
begin
  # Twitter scraper health check
  data, status_code, headers = api_instance.twitter_twitter_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_twitter_scraper_health_check_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_twitter_scraper_health_check_head

> Object twitter_twitter_scraper_health_check_head

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new

begin
  # Twitter scraper health check
  result = api_instance.twitter_twitter_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_twitter_scraper_health_check_head: #{e}"
end
```

#### Using the twitter_twitter_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> twitter_twitter_scraper_health_check_head_with_http_info

```ruby
begin
  # Twitter scraper health check
  data, status_code, headers = api_instance.twitter_twitter_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_twitter_scraper_health_check_head_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## twitter_update_filter_rule

> <FilterRuleResponse> twitter_update_filter_rule(rule_id, filter_rule_update)

Update filter rule

Partially update a filter rule.  Setting status='active' on a paused rule performs a credit check.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
rule_id = 'rule_id_example' # String | 
filter_rule_update = ScrapeBadger::FilterRuleUpdate.new # FilterRuleUpdate | 

begin
  # Update filter rule
  result = api_instance.twitter_update_filter_rule(rule_id, filter_rule_update)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_update_filter_rule: #{e}"
end
```

#### Using the twitter_update_filter_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FilterRuleResponse>, Integer, Hash)> twitter_update_filter_rule_with_http_info(rule_id, filter_rule_update)

```ruby
begin
  # Update filter rule
  data, status_code, headers = api_instance.twitter_update_filter_rule_with_http_info(rule_id, filter_rule_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FilterRuleResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_update_filter_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rule_id** | **String** |  |  |
| **filter_rule_update** | [**FilterRuleUpdate**](FilterRuleUpdate.md) |  |  |

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## twitter_update_stream_monitor

> <StreamMonitorResponse> twitter_update_stream_monitor(monitor_id, stream_monitor_update)

Update stream monitor

Partially update a stream monitor.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
monitor_id = 'monitor_id_example' # String | 
stream_monitor_update = ScrapeBadger::StreamMonitorUpdate.new # StreamMonitorUpdate | 

begin
  # Update stream monitor
  result = api_instance.twitter_update_stream_monitor(monitor_id, stream_monitor_update)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_update_stream_monitor: #{e}"
end
```

#### Using the twitter_update_stream_monitor_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StreamMonitorResponse>, Integer, Hash)> twitter_update_stream_monitor_with_http_info(monitor_id, stream_monitor_update)

```ruby
begin
  # Update stream monitor
  data, status_code, headers = api_instance.twitter_update_stream_monitor_with_http_info(monitor_id, stream_monitor_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StreamMonitorResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_update_stream_monitor_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monitor_id** | **String** |  |  |
| **stream_monitor_update** | [**StreamMonitorUpdate**](StreamMonitorUpdate.md) |  |  |

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## twitter_validate_search_query

> <FilterRuleValidateResponse> twitter_validate_search_query(filter_rule_validate_request)

Validate search query

Validate a Twitter search query string.  Performs basic structural validation without making a live Twitter request. Returns valid=True if the query passes syntax checks.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::TwitterApi.new
filter_rule_validate_request = ScrapeBadger::FilterRuleValidateRequest.new({query: 'query_example'}) # FilterRuleValidateRequest | 

begin
  # Validate search query
  result = api_instance.twitter_validate_search_query(filter_rule_validate_request)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_validate_search_query: #{e}"
end
```

#### Using the twitter_validate_search_query_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FilterRuleValidateResponse>, Integer, Hash)> twitter_validate_search_query_with_http_info(filter_rule_validate_request)

```ruby
begin
  # Validate search query
  data, status_code, headers = api_instance.twitter_validate_search_query_with_http_info(filter_rule_validate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FilterRuleValidateResponse>
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TwitterApi->twitter_validate_search_query_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **filter_rule_validate_request** | [**FilterRuleValidateRequest**](FilterRuleValidateRequest.md) |  |  |

### Return type

[**FilterRuleValidateResponse**](FilterRuleValidateResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

