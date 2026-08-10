# ScrapeBadger::YouTubeApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**youtube_batch_video_detail**](YouTubeApi.md#youtube_batch_video_detail) | **POST** /v1/youtube/videos/batch | Batch video detail |
| [**youtube_channel_about**](YouTubeApi.md#youtube_channel_about) | **GET** /v1/youtube/channels/{channel_id}/about | Channel about |
| [**youtube_channel_playlists**](YouTubeApi.md#youtube_channel_playlists) | **GET** /v1/youtube/channels/{channel_id}/playlists | Channel playlists |
| [**youtube_channel_shorts**](YouTubeApi.md#youtube_channel_shorts) | **GET** /v1/youtube/channels/{channel_id}/shorts | Channel shorts |
| [**youtube_channel_streams**](YouTubeApi.md#youtube_channel_streams) | **GET** /v1/youtube/channels/{channel_id}/streams | Channel streams |
| [**youtube_channel_videos**](YouTubeApi.md#youtube_channel_videos) | **GET** /v1/youtube/channels/{channel_id}/videos | Channel videos |
| [**youtube_comment_replies**](YouTubeApi.md#youtube_comment_replies) | **GET** /v1/youtube/videos/{video_id}/comments/{comment_id}/replies | Comment replies |
| [**youtube_community_post_comments**](YouTubeApi.md#youtube_community_post_comments) | **GET** /v1/youtube/posts/{post_id}/comments | Community post comments |
| [**youtube_community_posts**](YouTubeApi.md#youtube_community_posts) | **GET** /v1/youtube/channels/{channel_id}/community | Community posts |
| [**youtube_content_regions**](YouTubeApi.md#youtube_content_regions) | **GET** /v1/youtube/regions | Content regions |
| [**youtube_get_a_community_post**](YouTubeApi.md#youtube_get_a_community_post) | **GET** /v1/youtube/posts/{post_id} | Get a community post |
| [**youtube_get_a_mix_radio_queue**](YouTubeApi.md#youtube_get_a_mix_radio_queue) | **GET** /v1/youtube/mixes/{playlist_id} | Get a mix / radio queue |
| [**youtube_get_a_short**](YouTubeApi.md#youtube_get_a_short) | **GET** /v1/youtube/shorts/{video_id} | Get a Short |
| [**youtube_get_channel_detail**](YouTubeApi.md#youtube_get_channel_detail) | **GET** /v1/youtube/channels/{channel_id} | Get channel detail |
| [**youtube_get_playlist_detail**](YouTubeApi.md#youtube_get_playlist_detail) | **GET** /v1/youtube/playlists/{playlist_id} | Get playlist detail |
| [**youtube_get_video_detail**](YouTubeApi.md#youtube_get_video_detail) | **GET** /v1/youtube/videos/{video_id} | Get video detail |
| [**youtube_guest_home_feed**](YouTubeApi.md#youtube_guest_home_feed) | **GET** /v1/youtube/home | Guest home feed |
| [**youtube_keyword_suggestions**](YouTubeApi.md#youtube_keyword_suggestions) | **GET** /v1/youtube/autocomplete | Keyword suggestions |
| [**youtube_list_caption_tracks**](YouTubeApi.md#youtube_list_caption_tracks) | **GET** /v1/youtube/videos/{video_id}/captions | List caption tracks |
| [**youtube_live_chat_messages**](YouTubeApi.md#youtube_live_chat_messages) | **GET** /v1/youtube/videos/{video_id}/live_chat | Live chat messages |
| [**youtube_oembed_metadata**](YouTubeApi.md#youtube_oembed_metadata) | **GET** /v1/youtube/oembed | oEmbed metadata |
| [**youtube_playlist_items_page**](YouTubeApi.md#youtube_playlist_items_page) | **GET** /v1/youtube/playlists/{playlist_id}/items | Playlist items page |
| [**youtube_related_videos**](YouTubeApi.md#youtube_related_videos) | **GET** /v1/youtube/videos/{video_id}/related | Related videos |
| [**youtube_resolve_handle_url_to_id**](YouTubeApi.md#youtube_resolve_handle_url_to_id) | **GET** /v1/youtube/channels/resolve | Resolve handle/URL to id |
| [**youtube_search_within_a_channel**](YouTubeApi.md#youtube_search_within_a_channel) | **GET** /v1/youtube/channels/{channel_id}/search | Search within a channel |
| [**youtube_search_youtube**](YouTubeApi.md#youtube_search_youtube) | **GET** /v1/youtube/search | Search YouTube |
| [**youtube_search_youtube_music**](YouTubeApi.md#youtube_search_youtube_music) | **GET** /v1/youtube/music/search | Search YouTube Music |
| [**youtube_shorts_by_sound**](YouTubeApi.md#youtube_shorts_by_sound) | **GET** /v1/youtube/shorts/by_sound/{sound_id} | Shorts by sound |
| [**youtube_stream_formats**](YouTubeApi.md#youtube_stream_formats) | **GET** /v1/youtube/videos/{video_id}/streams | Stream formats |
| [**youtube_subscriber_count_fast**](YouTubeApi.md#youtube_subscriber_count_fast) | **GET** /v1/youtube/channels/{channel_id}/subscriber_count | Subscriber count (fast) |
| [**youtube_supported_markets**](YouTubeApi.md#youtube_supported_markets) | **GET** /v1/youtube/markets | Supported markets |
| [**youtube_trending_shorts**](YouTubeApi.md#youtube_trending_shorts) | **GET** /v1/youtube/trending/shorts | Trending shorts |
| [**youtube_trending_videos**](YouTubeApi.md#youtube_trending_videos) | **GET** /v1/youtube/trending | Trending videos |
| [**youtube_ui_languages**](YouTubeApi.md#youtube_ui_languages) | **GET** /v1/youtube/languages | UI languages |
| [**youtube_video_categories**](YouTubeApi.md#youtube_video_categories) | **GET** /v1/youtube/categories | Video categories |
| [**youtube_video_comments**](YouTubeApi.md#youtube_video_comments) | **GET** /v1/youtube/videos/{video_id}/comments | Video comments |
| [**youtube_video_transcript**](YouTubeApi.md#youtube_video_transcript) | **GET** /v1/youtube/videos/{video_id}/transcript | Video transcript |
| [**youtube_videos_under_a_hashtag**](YouTubeApi.md#youtube_videos_under_a_hashtag) | **GET** /v1/youtube/hashtags/{tag} | Videos under a hashtag |
| [**youtube_youtube_scraper_health_check**](YouTubeApi.md#youtube_youtube_scraper_health_check) | **GET** /v1/youtube/health | YouTube scraper health check |
| [**youtube_youtube_scraper_health_check_head**](YouTubeApi.md#youtube_youtube_scraper_health_check_head) | **HEAD** /v1/youtube/health | YouTube scraper health check |


## youtube_batch_video_detail

> Object youtube_batch_video_detail(request_body)

Batch video detail

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

api_instance = ScrapeBadger::YouTubeApi.new
request_body = { key: 3.56} # Hash<String, Object> | 

begin
  # Batch video detail
  result = api_instance.youtube_batch_video_detail(request_body)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_batch_video_detail: #{e}"
end
```

#### Using the youtube_batch_video_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_batch_video_detail_with_http_info(request_body)

```ruby
begin
  # Batch video detail
  data, status_code, headers = api_instance.youtube_batch_video_detail_with_http_info(request_body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_batch_video_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **request_body** | [**Hash&lt;String, Object&gt;**](Object.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## youtube_channel_about

> Object youtube_channel_about(channel_id)

Channel about

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

api_instance = ScrapeBadger::YouTubeApi.new
channel_id = 'channel_id_example' # String | 

begin
  # Channel about
  result = api_instance.youtube_channel_about(channel_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_about: #{e}"
end
```

#### Using the youtube_channel_about_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_channel_about_with_http_info(channel_id)

```ruby
begin
  # Channel about
  data, status_code, headers = api_instance.youtube_channel_about_with_http_info(channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_about_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_channel_playlists

> Object youtube_channel_playlists(channel_id)

Channel playlists

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

api_instance = ScrapeBadger::YouTubeApi.new
channel_id = 'channel_id_example' # String | 

begin
  # Channel playlists
  result = api_instance.youtube_channel_playlists(channel_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_playlists: #{e}"
end
```

#### Using the youtube_channel_playlists_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_channel_playlists_with_http_info(channel_id)

```ruby
begin
  # Channel playlists
  data, status_code, headers = api_instance.youtube_channel_playlists_with_http_info(channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_playlists_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_channel_shorts

> Object youtube_channel_shorts(channel_id)

Channel shorts

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

api_instance = ScrapeBadger::YouTubeApi.new
channel_id = 'channel_id_example' # String | 

begin
  # Channel shorts
  result = api_instance.youtube_channel_shorts(channel_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_shorts: #{e}"
end
```

#### Using the youtube_channel_shorts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_channel_shorts_with_http_info(channel_id)

```ruby
begin
  # Channel shorts
  data, status_code, headers = api_instance.youtube_channel_shorts_with_http_info(channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_shorts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_channel_streams

> Object youtube_channel_streams(channel_id)

Channel streams

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

api_instance = ScrapeBadger::YouTubeApi.new
channel_id = 'channel_id_example' # String | 

begin
  # Channel streams
  result = api_instance.youtube_channel_streams(channel_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_streams: #{e}"
end
```

#### Using the youtube_channel_streams_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_channel_streams_with_http_info(channel_id)

```ruby
begin
  # Channel streams
  data, status_code, headers = api_instance.youtube_channel_streams_with_http_info(channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_streams_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_channel_videos

> Object youtube_channel_videos(channel_id)

Channel videos

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

api_instance = ScrapeBadger::YouTubeApi.new
channel_id = 'channel_id_example' # String | 

begin
  # Channel videos
  result = api_instance.youtube_channel_videos(channel_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_videos: #{e}"
end
```

#### Using the youtube_channel_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_channel_videos_with_http_info(channel_id)

```ruby
begin
  # Channel videos
  data, status_code, headers = api_instance.youtube_channel_videos_with_http_info(channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_channel_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_comment_replies

> Object youtube_comment_replies(video_id, comment_id, continuation)

Comment replies

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

api_instance = ScrapeBadger::YouTubeApi.new
video_id = 'video_id_example' # String | 
comment_id = 'comment_id_example' # String | 
continuation = 'continuation_example' # String | Replies continuation token

begin
  # Comment replies
  result = api_instance.youtube_comment_replies(video_id, comment_id, continuation)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_comment_replies: #{e}"
end
```

#### Using the youtube_comment_replies_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_comment_replies_with_http_info(video_id, comment_id, continuation)

```ruby
begin
  # Comment replies
  data, status_code, headers = api_instance.youtube_comment_replies_with_http_info(video_id, comment_id, continuation)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_comment_replies_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **comment_id** | **String** |  |  |
| **continuation** | **String** | Replies continuation token |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_community_post_comments

> Object youtube_community_post_comments(post_id)

Community post comments

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

api_instance = ScrapeBadger::YouTubeApi.new
post_id = 'post_id_example' # String | 

begin
  # Community post comments
  result = api_instance.youtube_community_post_comments(post_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_community_post_comments: #{e}"
end
```

#### Using the youtube_community_post_comments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_community_post_comments_with_http_info(post_id)

```ruby
begin
  # Community post comments
  data, status_code, headers = api_instance.youtube_community_post_comments_with_http_info(post_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_community_post_comments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_community_posts

> Object youtube_community_posts(channel_id)

Community posts

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

api_instance = ScrapeBadger::YouTubeApi.new
channel_id = 'channel_id_example' # String | 

begin
  # Community posts
  result = api_instance.youtube_community_posts(channel_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_community_posts: #{e}"
end
```

#### Using the youtube_community_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_community_posts_with_http_info(channel_id)

```ruby
begin
  # Community posts
  data, status_code, headers = api_instance.youtube_community_posts_with_http_info(channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_community_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_content_regions

> Object youtube_content_regions

Content regions

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

api_instance = ScrapeBadger::YouTubeApi.new

begin
  # Content regions
  result = api_instance.youtube_content_regions
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_content_regions: #{e}"
end
```

#### Using the youtube_content_regions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_content_regions_with_http_info

```ruby
begin
  # Content regions
  data, status_code, headers = api_instance.youtube_content_regions_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_content_regions_with_http_info: #{e}"
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


## youtube_get_a_community_post

> Object youtube_get_a_community_post(post_id)

Get a community post

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

api_instance = ScrapeBadger::YouTubeApi.new
post_id = 'post_id_example' # String | 

begin
  # Get a community post
  result = api_instance.youtube_get_a_community_post(post_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_a_community_post: #{e}"
end
```

#### Using the youtube_get_a_community_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_get_a_community_post_with_http_info(post_id)

```ruby
begin
  # Get a community post
  data, status_code, headers = api_instance.youtube_get_a_community_post_with_http_info(post_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_a_community_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_get_a_mix_radio_queue

> Object youtube_get_a_mix_radio_queue(playlist_id)

Get a mix / radio queue

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

api_instance = ScrapeBadger::YouTubeApi.new
playlist_id = 'playlist_id_example' # String | 

begin
  # Get a mix / radio queue
  result = api_instance.youtube_get_a_mix_radio_queue(playlist_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_a_mix_radio_queue: #{e}"
end
```

#### Using the youtube_get_a_mix_radio_queue_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_get_a_mix_radio_queue_with_http_info(playlist_id)

```ruby
begin
  # Get a mix / radio queue
  data, status_code, headers = api_instance.youtube_get_a_mix_radio_queue_with_http_info(playlist_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_a_mix_radio_queue_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **playlist_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_get_a_short

> Object youtube_get_a_short(video_id)

Get a Short

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

api_instance = ScrapeBadger::YouTubeApi.new
video_id = 'video_id_example' # String | 

begin
  # Get a Short
  result = api_instance.youtube_get_a_short(video_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_a_short: #{e}"
end
```

#### Using the youtube_get_a_short_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_get_a_short_with_http_info(video_id)

```ruby
begin
  # Get a Short
  data, status_code, headers = api_instance.youtube_get_a_short_with_http_info(video_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_a_short_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_get_channel_detail

> Object youtube_get_channel_detail(channel_id, opts)

Get channel detail

Channel detail (accepts a UC id, @handle, or custom URL).

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

api_instance = ScrapeBadger::YouTubeApi.new
channel_id = 'channel_id_example' # String | 
opts = {
  gl: 'gl_example', # String | 
  hl: 'hl_example' # String | 
}

begin
  # Get channel detail
  result = api_instance.youtube_get_channel_detail(channel_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_channel_detail: #{e}"
end
```

#### Using the youtube_get_channel_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_get_channel_detail_with_http_info(channel_id, opts)

```ruby
begin
  # Get channel detail
  data, status_code, headers = api_instance.youtube_get_channel_detail_with_http_info(channel_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_channel_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |
| **gl** | **String** |  | [optional] |
| **hl** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_get_playlist_detail

> Object youtube_get_playlist_detail(playlist_id)

Get playlist detail

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

api_instance = ScrapeBadger::YouTubeApi.new
playlist_id = 'playlist_id_example' # String | 

begin
  # Get playlist detail
  result = api_instance.youtube_get_playlist_detail(playlist_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_playlist_detail: #{e}"
end
```

#### Using the youtube_get_playlist_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_get_playlist_detail_with_http_info(playlist_id)

```ruby
begin
  # Get playlist detail
  data, status_code, headers = api_instance.youtube_get_playlist_detail_with_http_info(playlist_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_playlist_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **playlist_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_get_video_detail

> Object youtube_get_video_detail(video_id, opts)

Get video detail

Full video detail — merged player + next (likes, comments, chapters, related).

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

api_instance = ScrapeBadger::YouTubeApi.new
video_id = 'video_id_example' # String | 
opts = {
  gl: 'gl_example', # String | 
  hl: 'hl_example' # String | 
}

begin
  # Get video detail
  result = api_instance.youtube_get_video_detail(video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_video_detail: #{e}"
end
```

#### Using the youtube_get_video_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_get_video_detail_with_http_info(video_id, opts)

```ruby
begin
  # Get video detail
  data, status_code, headers = api_instance.youtube_get_video_detail_with_http_info(video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_get_video_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **gl** | **String** |  | [optional] |
| **hl** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_guest_home_feed

> Object youtube_guest_home_feed

Guest home feed

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

api_instance = ScrapeBadger::YouTubeApi.new

begin
  # Guest home feed
  result = api_instance.youtube_guest_home_feed
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_guest_home_feed: #{e}"
end
```

#### Using the youtube_guest_home_feed_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_guest_home_feed_with_http_info

```ruby
begin
  # Guest home feed
  data, status_code, headers = api_instance.youtube_guest_home_feed_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_guest_home_feed_with_http_info: #{e}"
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


## youtube_keyword_suggestions

> Object youtube_keyword_suggestions(query, opts)

Keyword suggestions

Return YouTube keyword autocomplete suggestions.

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

api_instance = ScrapeBadger::YouTubeApi.new
query = 'query_example' # String | Partial query prefix
opts = {
  gl: 'gl_example', # String | 
  hl: 'hl_example' # String | 
}

begin
  # Keyword suggestions
  result = api_instance.youtube_keyword_suggestions(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_keyword_suggestions: #{e}"
end
```

#### Using the youtube_keyword_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_keyword_suggestions_with_http_info(query, opts)

```ruby
begin
  # Keyword suggestions
  data, status_code, headers = api_instance.youtube_keyword_suggestions_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_keyword_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial query prefix |  |
| **gl** | **String** |  | [optional] |
| **hl** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_list_caption_tracks

> Object youtube_list_caption_tracks(video_id)

List caption tracks

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

api_instance = ScrapeBadger::YouTubeApi.new
video_id = 'video_id_example' # String | 

begin
  # List caption tracks
  result = api_instance.youtube_list_caption_tracks(video_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_list_caption_tracks: #{e}"
end
```

#### Using the youtube_list_caption_tracks_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_list_caption_tracks_with_http_info(video_id)

```ruby
begin
  # List caption tracks
  data, status_code, headers = api_instance.youtube_list_caption_tracks_with_http_info(video_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_list_caption_tracks_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_live_chat_messages

> Object youtube_live_chat_messages(video_id, opts)

Live chat messages

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

api_instance = ScrapeBadger::YouTubeApi.new
video_id = 'video_id_example' # String | 
opts = {
  continuation: 'continuation_example', # String | 
  replay: true # Boolean | 
}

begin
  # Live chat messages
  result = api_instance.youtube_live_chat_messages(video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_live_chat_messages: #{e}"
end
```

#### Using the youtube_live_chat_messages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_live_chat_messages_with_http_info(video_id, opts)

```ruby
begin
  # Live chat messages
  data, status_code, headers = api_instance.youtube_live_chat_messages_with_http_info(video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_live_chat_messages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **continuation** | **String** |  | [optional] |
| **replay** | **Boolean** |  | [optional][default to false] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_oembed_metadata

> Object youtube_oembed_metadata(url)

oEmbed metadata

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

api_instance = ScrapeBadger::YouTubeApi.new
url = 'url_example' # String | A YouTube URL

begin
  # oEmbed metadata
  result = api_instance.youtube_oembed_metadata(url)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_oembed_metadata: #{e}"
end
```

#### Using the youtube_oembed_metadata_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_oembed_metadata_with_http_info(url)

```ruby
begin
  # oEmbed metadata
  data, status_code, headers = api_instance.youtube_oembed_metadata_with_http_info(url)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_oembed_metadata_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | A YouTube URL |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_playlist_items_page

> Object youtube_playlist_items_page(playlist_id)

Playlist items page

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

api_instance = ScrapeBadger::YouTubeApi.new
playlist_id = 'playlist_id_example' # String | 

begin
  # Playlist items page
  result = api_instance.youtube_playlist_items_page(playlist_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_playlist_items_page: #{e}"
end
```

#### Using the youtube_playlist_items_page_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_playlist_items_page_with_http_info(playlist_id)

```ruby
begin
  # Playlist items page
  data, status_code, headers = api_instance.youtube_playlist_items_page_with_http_info(playlist_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_playlist_items_page_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **playlist_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_related_videos

> Object youtube_related_videos(video_id)

Related videos

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

api_instance = ScrapeBadger::YouTubeApi.new
video_id = 'video_id_example' # String | 

begin
  # Related videos
  result = api_instance.youtube_related_videos(video_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_related_videos: #{e}"
end
```

#### Using the youtube_related_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_related_videos_with_http_info(video_id)

```ruby
begin
  # Related videos
  data, status_code, headers = api_instance.youtube_related_videos_with_http_info(video_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_related_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_resolve_handle_url_to_id

> Object youtube_resolve_handle_url_to_id(opts)

Resolve handle/URL to id

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

api_instance = ScrapeBadger::YouTubeApi.new
opts = {
  handle: 'handle_example', # String | 
  url: 'url_example' # String | 
}

begin
  # Resolve handle/URL to id
  result = api_instance.youtube_resolve_handle_url_to_id(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_resolve_handle_url_to_id: #{e}"
end
```

#### Using the youtube_resolve_handle_url_to_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_resolve_handle_url_to_id_with_http_info(opts)

```ruby
begin
  # Resolve handle/URL to id
  data, status_code, headers = api_instance.youtube_resolve_handle_url_to_id_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_resolve_handle_url_to_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **handle** | **String** |  | [optional] |
| **url** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_search_within_a_channel

> Object youtube_search_within_a_channel(channel_id, query)

Search within a channel

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

api_instance = ScrapeBadger::YouTubeApi.new
channel_id = 'channel_id_example' # String | 
query = 'query_example' # String | Search keywords

begin
  # Search within a channel
  result = api_instance.youtube_search_within_a_channel(channel_id, query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_search_within_a_channel: #{e}"
end
```

#### Using the youtube_search_within_a_channel_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_search_within_a_channel_with_http_info(channel_id, query)

```ruby
begin
  # Search within a channel
  data, status_code, headers = api_instance.youtube_search_within_a_channel_with_http_info(channel_id, query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_search_within_a_channel_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |
| **query** | **String** | Search keywords |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_search_youtube

> Object youtube_search_youtube(query, opts)

Search YouTube

Search videos / channels / playlists with the full filter matrix.

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

api_instance = ScrapeBadger::YouTubeApi.new
query = 'query_example' # String | Search keywords
opts = {
  type: 'type_example', # String | video|channel|playlist|movie|all
  sort_by: 'sort_by_example', # String | relevance|date|views|rating
  upload_date: 'upload_date_example', # String | hour|today|week|month|year
  duration: 'duration_example', # String | short|medium|long
  features: 'features_example', # String | hd,4k,360,vr180,3d,hdr,cc,subtitles,live
  gl: 'gl_example', # String | Content region (US, GB, DE…)
  hl: 'hl_example', # String | UI language
  continuation: 'continuation_example' # String | 
}

begin
  # Search YouTube
  result = api_instance.youtube_search_youtube(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_search_youtube: #{e}"
end
```

#### Using the youtube_search_youtube_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_search_youtube_with_http_info(query, opts)

```ruby
begin
  # Search YouTube
  data, status_code, headers = api_instance.youtube_search_youtube_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_search_youtube_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords |  |
| **type** | **String** | video|channel|playlist|movie|all | [optional] |
| **sort_by** | **String** | relevance|date|views|rating | [optional] |
| **upload_date** | **String** | hour|today|week|month|year | [optional] |
| **duration** | **String** | short|medium|long | [optional] |
| **features** | **String** | hd,4k,360,vr180,3d,hdr,cc,subtitles,live | [optional] |
| **gl** | **String** | Content region (US, GB, DE…) | [optional] |
| **hl** | **String** | UI language | [optional] |
| **continuation** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_search_youtube_music

> Object youtube_search_youtube_music(query)

Search YouTube Music

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

api_instance = ScrapeBadger::YouTubeApi.new
query = 'query_example' # String | Search keywords

begin
  # Search YouTube Music
  result = api_instance.youtube_search_youtube_music(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_search_youtube_music: #{e}"
end
```

#### Using the youtube_search_youtube_music_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_search_youtube_music_with_http_info(query)

```ruby
begin
  # Search YouTube Music
  data, status_code, headers = api_instance.youtube_search_youtube_music_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_search_youtube_music_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_shorts_by_sound

> Object youtube_shorts_by_sound(sound_id)

Shorts by sound

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

api_instance = ScrapeBadger::YouTubeApi.new
sound_id = 'sound_id_example' # String | 

begin
  # Shorts by sound
  result = api_instance.youtube_shorts_by_sound(sound_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_shorts_by_sound: #{e}"
end
```

#### Using the youtube_shorts_by_sound_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_shorts_by_sound_with_http_info(sound_id)

```ruby
begin
  # Shorts by sound
  data, status_code, headers = api_instance.youtube_shorts_by_sound_with_http_info(sound_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_shorts_by_sound_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sound_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_stream_formats

> Object youtube_stream_formats(video_id, opts)

Stream formats

Stream/format metadata (best-effort; media URLs may be PO-token gated).

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

api_instance = ScrapeBadger::YouTubeApi.new
video_id = 'video_id_example' # String | 
opts = {
  client: 'client_example' # String | IOS|ANDROID|WEB
}

begin
  # Stream formats
  result = api_instance.youtube_stream_formats(video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_stream_formats: #{e}"
end
```

#### Using the youtube_stream_formats_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_stream_formats_with_http_info(video_id, opts)

```ruby
begin
  # Stream formats
  data, status_code, headers = api_instance.youtube_stream_formats_with_http_info(video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_stream_formats_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **client** | **String** | IOS|ANDROID|WEB | [optional][default to &#39;IOS&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_subscriber_count_fast

> Object youtube_subscriber_count_fast(channel_id)

Subscriber count (fast)

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

api_instance = ScrapeBadger::YouTubeApi.new
channel_id = 'channel_id_example' # String | 

begin
  # Subscriber count (fast)
  result = api_instance.youtube_subscriber_count_fast(channel_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_subscriber_count_fast: #{e}"
end
```

#### Using the youtube_subscriber_count_fast_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_subscriber_count_fast_with_http_info(channel_id)

```ruby
begin
  # Subscriber count (fast)
  data, status_code, headers = api_instance.youtube_subscriber_count_fast_with_http_info(channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_subscriber_count_fast_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_supported_markets

> Object youtube_supported_markets

Supported markets

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

api_instance = ScrapeBadger::YouTubeApi.new

begin
  # Supported markets
  result = api_instance.youtube_supported_markets
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_supported_markets: #{e}"
end
```

#### Using the youtube_supported_markets_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_supported_markets_with_http_info

```ruby
begin
  # Supported markets
  data, status_code, headers = api_instance.youtube_supported_markets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_supported_markets_with_http_info: #{e}"
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


## youtube_trending_shorts

> Object youtube_trending_shorts

Trending shorts

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

api_instance = ScrapeBadger::YouTubeApi.new

begin
  # Trending shorts
  result = api_instance.youtube_trending_shorts
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_trending_shorts: #{e}"
end
```

#### Using the youtube_trending_shorts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_trending_shorts_with_http_info

```ruby
begin
  # Trending shorts
  data, status_code, headers = api_instance.youtube_trending_shorts_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_trending_shorts_with_http_info: #{e}"
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


## youtube_trending_videos

> Object youtube_trending_videos(opts)

Trending videos

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

api_instance = ScrapeBadger::YouTubeApi.new
opts = {
  gl: 'gl_example', # String | 
  type: 'type_example' # String | now|music|gaming|movies
}

begin
  # Trending videos
  result = api_instance.youtube_trending_videos(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_trending_videos: #{e}"
end
```

#### Using the youtube_trending_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_trending_videos_with_http_info(opts)

```ruby
begin
  # Trending videos
  data, status_code, headers = api_instance.youtube_trending_videos_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_trending_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gl** | **String** |  | [optional] |
| **type** | **String** | now|music|gaming|movies | [optional][default to &#39;now&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_ui_languages

> Object youtube_ui_languages

UI languages

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

api_instance = ScrapeBadger::YouTubeApi.new

begin
  # UI languages
  result = api_instance.youtube_ui_languages
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_ui_languages: #{e}"
end
```

#### Using the youtube_ui_languages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_ui_languages_with_http_info

```ruby
begin
  # UI languages
  data, status_code, headers = api_instance.youtube_ui_languages_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_ui_languages_with_http_info: #{e}"
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


## youtube_video_categories

> Object youtube_video_categories(opts)

Video categories

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

api_instance = ScrapeBadger::YouTubeApi.new
opts = {
  gl: 'gl_example' # String | 
}

begin
  # Video categories
  result = api_instance.youtube_video_categories(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_video_categories: #{e}"
end
```

#### Using the youtube_video_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_video_categories_with_http_info(opts)

```ruby
begin
  # Video categories
  data, status_code, headers = api_instance.youtube_video_categories_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_video_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gl** | **String** |  | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_video_comments

> Object youtube_video_comments(video_id, opts)

Video comments

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

api_instance = ScrapeBadger::YouTubeApi.new
video_id = 'video_id_example' # String | 
opts = {
  sort_by: 'sort_by_example', # String | top|newest
  continuation: 'continuation_example' # String | 
}

begin
  # Video comments
  result = api_instance.youtube_video_comments(video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_video_comments: #{e}"
end
```

#### Using the youtube_video_comments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_video_comments_with_http_info(video_id, opts)

```ruby
begin
  # Video comments
  data, status_code, headers = api_instance.youtube_video_comments_with_http_info(video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_video_comments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **sort_by** | **String** | top|newest | [optional][default to &#39;top&#39;] |
| **continuation** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_video_transcript

> Object youtube_video_transcript(video_id, opts)

Video transcript

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

api_instance = ScrapeBadger::YouTubeApi.new
video_id = 'video_id_example' # String | 
opts = {
  language: 'language_example' # String | BCP-47 language code
}

begin
  # Video transcript
  result = api_instance.youtube_video_transcript(video_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_video_transcript: #{e}"
end
```

#### Using the youtube_video_transcript_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_video_transcript_with_http_info(video_id, opts)

```ruby
begin
  # Video transcript
  data, status_code, headers = api_instance.youtube_video_transcript_with_http_info(video_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_video_transcript_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **video_id** | **String** |  |  |
| **language** | **String** | BCP-47 language code | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_videos_under_a_hashtag

> Object youtube_videos_under_a_hashtag(tag)

Videos under a hashtag

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

api_instance = ScrapeBadger::YouTubeApi.new
tag = 'tag_example' # String | 

begin
  # Videos under a hashtag
  result = api_instance.youtube_videos_under_a_hashtag(tag)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_videos_under_a_hashtag: #{e}"
end
```

#### Using the youtube_videos_under_a_hashtag_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_videos_under_a_hashtag_with_http_info(tag)

```ruby
begin
  # Videos under a hashtag
  data, status_code, headers = api_instance.youtube_videos_under_a_hashtag_with_http_info(tag)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_videos_under_a_hashtag_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tag** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## youtube_youtube_scraper_health_check

> Object youtube_youtube_scraper_health_check

YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::YouTubeApi.new

begin
  # YouTube scraper health check
  result = api_instance.youtube_youtube_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_youtube_scraper_health_check: #{e}"
end
```

#### Using the youtube_youtube_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_youtube_scraper_health_check_with_http_info

```ruby
begin
  # YouTube scraper health check
  data, status_code, headers = api_instance.youtube_youtube_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_youtube_scraper_health_check_with_http_info: #{e}"
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


## youtube_youtube_scraper_health_check_head

> Object youtube_youtube_scraper_health_check_head

YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::YouTubeApi.new

begin
  # YouTube scraper health check
  result = api_instance.youtube_youtube_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_youtube_scraper_health_check_head: #{e}"
end
```

#### Using the youtube_youtube_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> youtube_youtube_scraper_health_check_head_with_http_info

```ruby
begin
  # YouTube scraper health check
  data, status_code, headers = api_instance.youtube_youtube_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling YouTubeApi->youtube_youtube_scraper_health_check_head_with_http_info: #{e}"
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

