# ScrapeBadger::TikTokApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**tiktok_general_search**](TikTokApi.md#tiktok_general_search) | **GET** /v1/tiktok/search | General search |
| [**tiktok_get_comment_replies**](TikTokApi.md#tiktok_get_comment_replies) | **GET** /v1/tiktok/comments/{comment_id}/replies | Get comment replies |
| [**tiktok_get_comments**](TikTokApi.md#tiktok_get_comments) | **GET** /v1/tiktok/videos/{video_id}/comments | Get comments |
| [**tiktok_get_followers_deprecated**](TikTokApi.md#tiktok_get_followers_deprecated) | **GET** /v1/tiktok/users/{username}/followers | Get followers (deprecated) |
| [**tiktok_get_following_deprecated**](TikTokApi.md#tiktok_get_following_deprecated) | **GET** /v1/tiktok/users/{username}/following | Get following (deprecated) |
| [**tiktok_get_hashtag_detail**](TikTokApi.md#tiktok_get_hashtag_detail) | **GET** /v1/tiktok/hashtags/{name} | Get hashtag detail |
| [**tiktok_get_hashtag_videos**](TikTokApi.md#tiktok_get_hashtag_videos) | **GET** /v1/tiktok/hashtags/{name}/videos | Get hashtag videos |
| [**tiktok_get_liked_videos_deprecated**](TikTokApi.md#tiktok_get_liked_videos_deprecated) | **GET** /v1/tiktok/users/{username}/liked | Get liked videos (deprecated) |
| [**tiktok_get_music_sound_detail**](TikTokApi.md#tiktok_get_music_sound_detail) | **GET** /v1/tiktok/music/{music_id} | Get music/sound detail |
| [**tiktok_get_music_videos**](TikTokApi.md#tiktok_get_music_videos) | **GET** /v1/tiktok/music/{music_id}/videos | Get music videos |
| [**tiktok_get_oembed_metadata**](TikTokApi.md#tiktok_get_oembed_metadata) | **GET** /v1/tiktok/oembed | Get oEmbed metadata |
| [**tiktok_get_related_videos**](TikTokApi.md#tiktok_get_related_videos) | **GET** /v1/tiktok/videos/{video_id}/related | Get related videos |
| [**tiktok_get_reposts**](TikTokApi.md#tiktok_get_reposts) | **GET** /v1/tiktok/users/{username}/reposts | Get reposts |
| [**tiktok_get_tiktok_ad_detail**](TikTokApi.md#tiktok_get_tiktok_ad_detail) | **GET** /v1/tiktok/ads/{ad_id} | Get TikTok ad detail |
| [**tiktok_get_transcript**](TikTokApi.md#tiktok_get_transcript) | **GET** /v1/tiktok/videos/{video_id}/transcript | Get transcript |
| [**tiktok_get_user_profile**](TikTokApi.md#tiktok_get_user_profile) | **GET** /v1/tiktok/users/{username} | Get user profile |
| [**tiktok_get_user_videos**](TikTokApi.md#tiktok_get_user_videos) | **GET** /v1/tiktok/users/{username}/videos | Get user videos |
| [**tiktok_get_video_detail**](TikTokApi.md#tiktok_get_video_detail) | **GET** /v1/tiktok/videos/{video_id} | Get video detail |
| [**tiktok_health_check**](TikTokApi.md#tiktok_health_check) | **GET** /v1/tiktok/health | Health check |
| [**tiktok_health_check_head**](TikTokApi.md#tiktok_health_check_head) | **HEAD** /v1/tiktok/health | Health check |
| [**tiktok_list_regions**](TikTokApi.md#tiktok_list_regions) | **GET** /v1/tiktok/regions | List regions |
| [**tiktok_search_hashtags**](TikTokApi.md#tiktok_search_hashtags) | **GET** /v1/tiktok/search/hashtags | Search hashtags |
| [**tiktok_search_the_tiktok_ad_library**](TikTokApi.md#tiktok_search_the_tiktok_ad_library) | **GET** /v1/tiktok/ads/search | Search the TikTok Ad Library |
| [**tiktok_search_tiktok_advertisers**](TikTokApi.md#tiktok_search_tiktok_advertisers) | **GET** /v1/tiktok/ads/advertisers | Search TikTok advertisers |
| [**tiktok_search_users**](TikTokApi.md#tiktok_search_users) | **GET** /v1/tiktok/search/users | Search users |
| [**tiktok_search_videos**](TikTokApi.md#tiktok_search_videos) | **GET** /v1/tiktok/search/videos | Search videos |
| [**tiktok_trending_hashtags**](TikTokApi.md#tiktok_trending_hashtags) | **GET** /v1/tiktok/trending/hashtags | Trending hashtags |
| [**tiktok_trending_songs**](TikTokApi.md#tiktok_trending_songs) | **GET** /v1/tiktok/trending/songs | Trending songs |
| [**tiktok_trending_videos**](TikTokApi.md#tiktok_trending_videos) | **GET** /v1/tiktok/trending/videos | Trending videos |


## tiktok_general_search

> Object tiktok_general_search(query, opts)

General search

General TikTok search — video results from the Top feed.

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

api_instance = ScrapeBadger::TikTokApi.new
query = 'query_example' # String | Search keyword
opts = {
  region: 'region_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor
}

begin
  # General search
  result = api_instance.tiktok_general_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_general_search: #{e}"
end
```

#### Using the tiktok_general_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_general_search_with_http_info(query, opts)

```ruby
begin
  # General search
  data, status_code, headers = api_instance.tiktok_general_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_general_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keyword |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_comment_replies

> Object tiktok_get_comment_replies(comment_id, video_id, opts)

Get comment replies

Get replies to a TikTok comment (best-effort).

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

api_instance = ScrapeBadger::TikTokApi.new
comment_id = 'comment_id_example' # String | 
video_id = 'video_id_example' # String | Parent video id
opts = {
  region: 'region_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | Pagination cursor from a prior page's pagination.cursor
}

begin
  # Get comment replies
  result = api_instance.tiktok_get_comment_replies(comment_id, video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_comment_replies: #{e}"
end
```

#### Using the tiktok_get_comment_replies_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_comment_replies_with_http_info(comment_id, video_id, opts)

```ruby
begin
  # Get comment replies
  data, status_code, headers = api_instance.tiktok_get_comment_replies_with_http_info(comment_id, video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_comment_replies_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **comment_id** | **String** |  |  |
| **video_id** | **String** | Parent video id |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_comments

> Object tiktok_get_comments(video_id, opts)

Get comments

Get top-level comments on a TikTok video.

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

api_instance = ScrapeBadger::TikTokApi.new
video_id = 'video_id_example' # String | 
opts = {
  region: 'region_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | Pagination cursor from a prior page's pagination.cursor
}

begin
  # Get comments
  result = api_instance.tiktok_get_comments(video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_comments: #{e}"
end
```

#### Using the tiktok_get_comments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_comments_with_http_info(video_id, opts)

```ruby
begin
  # Get comments
  data, status_code, headers = api_instance.tiktok_get_comments_with_http_info(video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_comments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_followers_deprecated

> Object tiktok_get_followers_deprecated(username, opts)

Get followers (deprecated)

DEPRECATED — TikTok followers require an authenticated account session. Returns HTTP 410.

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

api_instance = ScrapeBadger::TikTokApi.new
username = 'username_example' # String | 
opts = {
  region: 'region_example', # String | 
  count: 56 # Integer | 
}

begin
  # Get followers (deprecated)
  result = api_instance.tiktok_get_followers_deprecated(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_followers_deprecated: #{e}"
end
```

#### Using the tiktok_get_followers_deprecated_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_followers_deprecated_with_http_info(username, opts)

```ruby
begin
  # Get followers (deprecated)
  data, status_code, headers = api_instance.tiktok_get_followers_deprecated_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_followers_deprecated_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 30] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_following_deprecated

> Object tiktok_get_following_deprecated(username, opts)

Get following (deprecated)

DEPRECATED — TikTok following requires an authenticated account session. Returns HTTP 410.

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

api_instance = ScrapeBadger::TikTokApi.new
username = 'username_example' # String | 
opts = {
  region: 'region_example', # String | 
  count: 56 # Integer | 
}

begin
  # Get following (deprecated)
  result = api_instance.tiktok_get_following_deprecated(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_following_deprecated: #{e}"
end
```

#### Using the tiktok_get_following_deprecated_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_following_deprecated_with_http_info(username, opts)

```ruby
begin
  # Get following (deprecated)
  data, status_code, headers = api_instance.tiktok_get_following_deprecated_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_following_deprecated_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 30] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_hashtag_detail

> Object tiktok_get_hashtag_detail(name, opts)

Get hashtag detail

Get TikTok hashtag/challenge detail.

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

api_instance = ScrapeBadger::TikTokApi.new
name = 'name_example' # String | 
opts = {
  region: 'region_example' # String | 
}

begin
  # Get hashtag detail
  result = api_instance.tiktok_get_hashtag_detail(name, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_hashtag_detail: #{e}"
end
```

#### Using the tiktok_get_hashtag_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_hashtag_detail_with_http_info(name, opts)

```ruby
begin
  # Get hashtag detail
  data, status_code, headers = api_instance.tiktok_get_hashtag_detail_with_http_info(name, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_hashtag_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_hashtag_videos

> Object tiktok_get_hashtag_videos(name, opts)

Get hashtag videos

Get videos tagged with a TikTok hashtag.

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

api_instance = ScrapeBadger::TikTokApi.new
name = 'name_example' # String | 
opts = {
  region: 'region_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | Pagination cursor from a prior page's pagination.cursor
}

begin
  # Get hashtag videos
  result = api_instance.tiktok_get_hashtag_videos(name, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_hashtag_videos: #{e}"
end
```

#### Using the tiktok_get_hashtag_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_hashtag_videos_with_http_info(name, opts)

```ruby
begin
  # Get hashtag videos
  data, status_code, headers = api_instance.tiktok_get_hashtag_videos_with_http_info(name, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_hashtag_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 30] |
| **cursor** | **String** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_liked_videos_deprecated

> Object tiktok_get_liked_videos_deprecated(username, opts)

Get liked videos (deprecated)

DEPRECATED — TikTok liked videos require an authenticated account session. Returns HTTP 410.

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

api_instance = ScrapeBadger::TikTokApi.new
username = 'username_example' # String | 
opts = {
  region: 'region_example', # String | 
  count: 56 # Integer | 
}

begin
  # Get liked videos (deprecated)
  result = api_instance.tiktok_get_liked_videos_deprecated(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_liked_videos_deprecated: #{e}"
end
```

#### Using the tiktok_get_liked_videos_deprecated_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_liked_videos_deprecated_with_http_info(username, opts)

```ruby
begin
  # Get liked videos (deprecated)
  data, status_code, headers = api_instance.tiktok_get_liked_videos_deprecated_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_liked_videos_deprecated_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 30] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_music_sound_detail

> Object tiktok_get_music_sound_detail(music_id, opts)

Get music/sound detail

Get TikTok sound/music detail.

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

api_instance = ScrapeBadger::TikTokApi.new
music_id = 'music_id_example' # String | 
opts = {
  region: 'region_example' # String | 
}

begin
  # Get music/sound detail
  result = api_instance.tiktok_get_music_sound_detail(music_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_music_sound_detail: #{e}"
end
```

#### Using the tiktok_get_music_sound_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_music_sound_detail_with_http_info(music_id, opts)

```ruby
begin
  # Get music/sound detail
  data, status_code, headers = api_instance.tiktok_get_music_sound_detail_with_http_info(music_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_music_sound_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **music_id** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_music_videos

> Object tiktok_get_music_videos(music_id, opts)

Get music videos

Get videos using a given TikTok sound.

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

api_instance = ScrapeBadger::TikTokApi.new
music_id = 'music_id_example' # String | 
opts = {
  region: 'region_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | Pagination cursor from a prior page's pagination.cursor
}

begin
  # Get music videos
  result = api_instance.tiktok_get_music_videos(music_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_music_videos: #{e}"
end
```

#### Using the tiktok_get_music_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_music_videos_with_http_info(music_id, opts)

```ruby
begin
  # Get music videos
  data, status_code, headers = api_instance.tiktok_get_music_videos_with_http_info(music_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_music_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **music_id** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 30] |
| **cursor** | **String** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_oembed_metadata

> Object tiktok_get_oembed_metadata(url, opts)

Get oEmbed metadata

Get cheap unauthenticated oEmbed metadata for a TikTok URL.

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

api_instance = ScrapeBadger::TikTokApi.new
url = 'url_example' # String | Full TikTok video or profile URL
opts = {
  region: 'region_example' # String | 
}

begin
  # Get oEmbed metadata
  result = api_instance.tiktok_get_oembed_metadata(url, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_oembed_metadata: #{e}"
end
```

#### Using the tiktok_get_oembed_metadata_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_oembed_metadata_with_http_info(url, opts)

```ruby
begin
  # Get oEmbed metadata
  data, status_code, headers = api_instance.tiktok_get_oembed_metadata_with_http_info(url, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_oembed_metadata_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Full TikTok video or profile URL |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_related_videos

> Object tiktok_get_related_videos(video_id, opts)

Get related videos

Get TikTok's related videos for a given video.

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

api_instance = ScrapeBadger::TikTokApi.new
video_id = 'video_id_example' # String | 
opts = {
  region: 'region_example', # String | 
  count: 56 # Integer | 
}

begin
  # Get related videos
  result = api_instance.tiktok_get_related_videos(video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_related_videos: #{e}"
end
```

#### Using the tiktok_get_related_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_related_videos_with_http_info(video_id, opts)

```ruby
begin
  # Get related videos
  data, status_code, headers = api_instance.tiktok_get_related_videos_with_http_info(video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_related_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 16] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_reposts

> Object tiktok_get_reposts(username, opts)

Get reposts

Get videos a TikTok user has reposted.

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

api_instance = ScrapeBadger::TikTokApi.new
username = 'username_example' # String | 
opts = {
  region: 'region_example', # String | 
  count: 56 # Integer | 
}

begin
  # Get reposts
  result = api_instance.tiktok_get_reposts(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_reposts: #{e}"
end
```

#### Using the tiktok_get_reposts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_reposts_with_http_info(username, opts)

```ruby
begin
  # Get reposts
  data, status_code, headers = api_instance.tiktok_get_reposts_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_reposts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 30] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_tiktok_ad_detail

> Object tiktok_get_tiktok_ad_detail(ad_id, opts)

Get TikTok ad detail

Get a single ad's advertiser, creatives, and targeting/impression breakdown.

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

api_instance = ScrapeBadger::TikTokApi.new
ad_id = 'ad_id_example' # String | 
opts = {
  region: 'region_example' # String | EU region code (the Ad Library is EU-only)
}

begin
  # Get TikTok ad detail
  result = api_instance.tiktok_get_tiktok_ad_detail(ad_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_tiktok_ad_detail: #{e}"
end
```

#### Using the tiktok_get_tiktok_ad_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_tiktok_ad_detail_with_http_info(ad_id, opts)

```ruby
begin
  # Get TikTok ad detail
  data, status_code, headers = api_instance.tiktok_get_tiktok_ad_detail_with_http_info(ad_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_tiktok_ad_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ad_id** | **String** |  |  |
| **region** | **String** | EU region code (the Ad Library is EU-only) | [optional][default to &#39;DE&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_transcript

> Object tiktok_get_transcript(video_id, opts)

Get transcript

Get subtitle/caption tracks for a TikTok video.

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

api_instance = ScrapeBadger::TikTokApi.new
video_id = 'video_id_example' # String | 
opts = {
  region: 'region_example' # String | 
}

begin
  # Get transcript
  result = api_instance.tiktok_get_transcript(video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_transcript: #{e}"
end
```

#### Using the tiktok_get_transcript_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_transcript_with_http_info(video_id, opts)

```ruby
begin
  # Get transcript
  data, status_code, headers = api_instance.tiktok_get_transcript_with_http_info(video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_transcript_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_user_profile

> Object tiktok_get_user_profile(username, opts)

Get user profile

Get a TikTok user's full profile.

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

api_instance = ScrapeBadger::TikTokApi.new
username = 'username_example' # String | 
opts = {
  region: 'region_example' # String | Content region (ISO 3166-1 alpha-2)
}

begin
  # Get user profile
  result = api_instance.tiktok_get_user_profile(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_user_profile: #{e}"
end
```

#### Using the tiktok_get_user_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_user_profile_with_http_info(username, opts)

```ruby
begin
  # Get user profile
  data, status_code, headers = api_instance.tiktok_get_user_profile_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_user_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **region** | **String** | Content region (ISO 3166-1 alpha-2) | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_user_videos

> Object tiktok_get_user_videos(username, opts)

Get user videos

Get a TikTok user's posted videos.

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

api_instance = ScrapeBadger::TikTokApi.new
username = 'username_example' # String | 
opts = {
  region: 'region_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | Pagination cursor from a prior page's `pagination.cursor` (signer path only).
}

begin
  # Get user videos
  result = api_instance.tiktok_get_user_videos(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_user_videos: #{e}"
end
```

#### Using the tiktok_get_user_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_user_videos_with_http_info(username, opts)

```ruby
begin
  # Get user videos
  data, status_code, headers = api_instance.tiktok_get_user_videos_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_user_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 30] |
| **cursor** | **String** | Pagination cursor from a prior page&#39;s &#x60;pagination.cursor&#x60; (signer path only). | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_get_video_detail

> Object tiktok_get_video_detail(video_id, opts)

Get video detail

Get full metadata for a single TikTok video/post.

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

api_instance = ScrapeBadger::TikTokApi.new
video_id = 'video_id_example' # String | 
opts = {
  region: 'region_example', # String | 
  username: 'username_example' # String | Author handle (skips oEmbed lookup)
}

begin
  # Get video detail
  result = api_instance.tiktok_get_video_detail(video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_video_detail: #{e}"
end
```

#### Using the tiktok_get_video_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_get_video_detail_with_http_info(video_id, opts)

```ruby
begin
  # Get video detail
  data, status_code, headers = api_instance.tiktok_get_video_detail_with_http_info(video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_get_video_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **username** | **String** | Author handle (skips oEmbed lookup) | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_health_check

> Object tiktok_health_check

Health check

Check health of the TikTok scraper service.

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

api_instance = ScrapeBadger::TikTokApi.new

begin
  # Health check
  result = api_instance.tiktok_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_health_check: #{e}"
end
```

#### Using the tiktok_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_health_check_with_http_info

```ruby
begin
  # Health check
  data, status_code, headers = api_instance.tiktok_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_health_check_with_http_info: #{e}"
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


## tiktok_health_check_head

> Object tiktok_health_check_head

Health check

Check health of the TikTok scraper service.

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

api_instance = ScrapeBadger::TikTokApi.new

begin
  # Health check
  result = api_instance.tiktok_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_health_check_head: #{e}"
end
```

#### Using the tiktok_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_health_check_head_with_http_info

```ruby
begin
  # Health check
  data, status_code, headers = api_instance.tiktok_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_health_check_head_with_http_info: #{e}"
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


## tiktok_list_regions

> Object tiktok_list_regions

List regions

List supported TikTok content regions.

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

api_instance = ScrapeBadger::TikTokApi.new

begin
  # List regions
  result = api_instance.tiktok_list_regions
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_list_regions: #{e}"
end
```

#### Using the tiktok_list_regions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_list_regions_with_http_info

```ruby
begin
  # List regions
  data, status_code, headers = api_instance.tiktok_list_regions_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_list_regions_with_http_info: #{e}"
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


## tiktok_search_hashtags

> Object tiktok_search_hashtags(query, opts)

Search hashtags

Search TikTok hashtags by keyword.

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

api_instance = ScrapeBadger::TikTokApi.new
query = 'query_example' # String | Search keyword
opts = {
  region: 'region_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor
}

begin
  # Search hashtags
  result = api_instance.tiktok_search_hashtags(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_hashtags: #{e}"
end
```

#### Using the tiktok_search_hashtags_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_search_hashtags_with_http_info(query, opts)

```ruby
begin
  # Search hashtags
  data, status_code, headers = api_instance.tiktok_search_hashtags_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_hashtags_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keyword |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_search_the_tiktok_ad_library

> Object tiktok_search_the_tiktok_ad_library(opts)

Search the TikTok Ad Library

Search TikTok's Commercial Content Library (ad transparency) by keyword or advertiser.

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

api_instance = ScrapeBadger::TikTokApi.new
opts = {
  query: 'query_example', # String | Keyword (ignored when advertiser_id is set)
  advertiser_id: 'advertiser_id_example', # String | Advertiser business id(s) for advertiser search
  region: 'region_example', # String | EU region code (the Ad Library is EU-only)
  days: 56, # Integer | 
  sort: 'sort_example', # String | 
  offset: 56, # Integer | 
  search_id: 'search_id_example', # String | 
  count: 56 # Integer | 
}

begin
  # Search the TikTok Ad Library
  result = api_instance.tiktok_search_the_tiktok_ad_library(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_the_tiktok_ad_library: #{e}"
end
```

#### Using the tiktok_search_the_tiktok_ad_library_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_search_the_tiktok_ad_library_with_http_info(opts)

```ruby
begin
  # Search the TikTok Ad Library
  data, status_code, headers = api_instance.tiktok_search_the_tiktok_ad_library_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_the_tiktok_ad_library_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Keyword (ignored when advertiser_id is set) | [optional][default to &#39;&#39;] |
| **advertiser_id** | **String** | Advertiser business id(s) for advertiser search | [optional][default to &#39;&#39;] |
| **region** | **String** | EU region code (the Ad Library is EU-only) | [optional][default to &#39;DE&#39;] |
| **days** | **Integer** |  | [optional][default to 30] |
| **sort** | **String** |  | [optional][default to &#39;last_shown_date,desc&#39;] |
| **offset** | **Integer** |  | [optional][default to 0] |
| **search_id** | **String** |  | [optional][default to &#39;&#39;] |
| **count** | **Integer** |  | [optional][default to 20] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_search_tiktok_advertisers

> Object tiktok_search_tiktok_advertisers(query, opts)

Search TikTok advertisers

Look up TikTok advertiser business ids by name (feeds ads/search?advertiser_id=).

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

api_instance = ScrapeBadger::TikTokApi.new
query = 'query_example' # String | Advertiser name (or partial) to look up
opts = {
  region: 'region_example', # String | EU region code (the Ad Library is EU-only)
  count: 56 # Integer | 
}

begin
  # Search TikTok advertisers
  result = api_instance.tiktok_search_tiktok_advertisers(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_tiktok_advertisers: #{e}"
end
```

#### Using the tiktok_search_tiktok_advertisers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_search_tiktok_advertisers_with_http_info(query, opts)

```ruby
begin
  # Search TikTok advertisers
  data, status_code, headers = api_instance.tiktok_search_tiktok_advertisers_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_tiktok_advertisers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Advertiser name (or partial) to look up |  |
| **region** | **String** | EU region code (the Ad Library is EU-only) | [optional][default to &#39;DE&#39;] |
| **count** | **Integer** |  | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_search_users

> Object tiktok_search_users(query, opts)

Search users

Search TikTok users by keyword.

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

api_instance = ScrapeBadger::TikTokApi.new
query = 'query_example' # String | Search keyword
opts = {
  region: 'region_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor
}

begin
  # Search users
  result = api_instance.tiktok_search_users(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_users: #{e}"
end
```

#### Using the tiktok_search_users_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_search_users_with_http_info(query, opts)

```ruby
begin
  # Search users
  data, status_code, headers = api_instance.tiktok_search_users_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_users_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keyword |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_search_videos

> Object tiktok_search_videos(query, opts)

Search videos

Search TikTok videos by keyword.

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

api_instance = ScrapeBadger::TikTokApi.new
query = 'query_example' # String | Search keyword
opts = {
  region: 'region_example', # String | 
  count: 56, # Integer | 
  cursor: 'cursor_example' # String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor
}

begin
  # Search videos
  result = api_instance.tiktok_search_videos(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_videos: #{e}"
end
```

#### Using the tiktok_search_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_search_videos_with_http_info(query, opts)

```ruby
begin
  # Search videos
  data, status_code, headers = api_instance.tiktok_search_videos_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_search_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keyword |  |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_trending_hashtags

> Object tiktok_trending_hashtags(opts)

Trending hashtags

Get trending hashtags (mobile Discover surface — view_count + creators).

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

api_instance = ScrapeBadger::TikTokApi.new
opts = {
  region: 'region_example', # String | 
  period: 56, # Integer | 
  count: 56 # Integer | 
}

begin
  # Trending hashtags
  result = api_instance.tiktok_trending_hashtags(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_trending_hashtags: #{e}"
end
```

#### Using the tiktok_trending_hashtags_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_trending_hashtags_with_http_info(opts)

```ruby
begin
  # Trending hashtags
  data, status_code, headers = api_instance.tiktok_trending_hashtags_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_trending_hashtags_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **period** | **Integer** |  | [optional][default to 7] |
| **count** | **Integer** |  | [optional][default to 20] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_trending_songs

> Object tiktok_trending_songs(opts)

Trending songs

Get trending songs/sounds (mobile hot-music feed — ranked by usage).

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

api_instance = ScrapeBadger::TikTokApi.new
opts = {
  region: 'region_example', # String | 
  period: 56, # Integer | 
  count: 56 # Integer | 
}

begin
  # Trending songs
  result = api_instance.tiktok_trending_songs(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_trending_songs: #{e}"
end
```

#### Using the tiktok_trending_songs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_trending_songs_with_http_info(opts)

```ruby
begin
  # Trending songs
  data, status_code, headers = api_instance.tiktok_trending_songs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_trending_songs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **period** | **Integer** |  | [optional][default to 7] |
| **count** | **Integer** |  | [optional][default to 20] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tiktok_trending_videos

> Object tiktok_trending_videos(opts)

Trending videos

Get trending videos from the TikTok Explore feed.

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

api_instance = ScrapeBadger::TikTokApi.new
opts = {
  region: 'region_example', # String | 
  count: 56 # Integer | 
}

begin
  # Trending videos
  result = api_instance.tiktok_trending_videos(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_trending_videos: #{e}"
end
```

#### Using the tiktok_trending_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> tiktok_trending_videos_with_http_info(opts)

```ruby
begin
  # Trending videos
  data, status_code, headers = api_instance.tiktok_trending_videos_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling TikTokApi->tiktok_trending_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **region** | **String** |  | [optional][default to &#39;US&#39;] |
| **count** | **Integer** |  | [optional][default to 20] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

