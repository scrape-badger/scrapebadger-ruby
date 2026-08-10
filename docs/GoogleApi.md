# ScrapeBadger::GoogleApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**google_get_author_citations_per_year_chart**](GoogleApi.md#google_get_author_citations_per_year_chart) | **GET** /v1/google/scholar/author/citation | Get author citations-per-year chart |
| [**google_get_business_posts**](GoogleApi.md#google_get_business_posts) | **GET** /v1/google/maps/posts | Get business posts |
| [**google_get_citation_formats_for_a_scholar_paper**](GoogleApi.md#google_get_citation_formats_for_a_scholar_paper) | **GET** /v1/google/scholar/cite | Get citation formats for a Scholar paper |
| [**google_get_place_details**](GoogleApi.md#google_get_place_details) | **GET** /v1/google/maps/place | Get place details |
| [**google_get_place_photos**](GoogleApi.md#google_get_place_photos) | **GET** /v1/google/maps/photos | Get place photos |
| [**google_get_place_reviews**](GoogleApi.md#google_get_place_reviews) | **GET** /v1/google/maps/reviews | Get place reviews |
| [**google_get_scholar_author_profile**](GoogleApi.md#google_get_scholar_author_profile) | **GET** /v1/google/scholar/author | Get Scholar author profile |
| [**google_get_stock_index_quote**](GoogleApi.md#google_get_stock_index_quote) | **GET** /v1/google/finance/quote | Get stock/index quote |
| [**google_google_ai_mode_search**](GoogleApi.md#google_google_ai_mode_search) | **GET** /v1/google/ai-mode/search | Google AI Mode search |
| [**google_google_ai_overview_inline_serp_block**](GoogleApi.md#google_google_ai_overview_inline_serp_block) | **GET** /v1/google/ai-overview | Google AI Overview (inline SERP block) |
| [**google_google_flights_calendar_cheapest_fare_per_date**](GoogleApi.md#google_google_flights_calendar_cheapest_fare_per_date) | **GET** /v1/google/flights/calendar | Google Flights calendar — cheapest fare per date |
| [**google_google_flights_search**](GoogleApi.md#google_google_flights_search) | **GET** /v1/google/flights/search | Google Flights search |
| [**google_google_lens_visual_search**](GoogleApi.md#google_google_lens_visual_search) | **GET** /v1/google/lens/search | Google Lens visual search |
| [**google_google_scraper_health_check**](GoogleApi.md#google_google_scraper_health_check) | **GET** /v1/google/health | Google scraper health check |
| [**google_google_scraper_health_check_head**](GoogleApi.md#google_google_scraper_health_check_head) | **HEAD** /v1/google/health | Google scraper health check |
| [**google_google_search_suggestions**](GoogleApi.md#google_google_search_suggestions) | **GET** /v1/google/autocomplete | Google search suggestions |
| [**google_google_shorts_search**](GoogleApi.md#google_google_shorts_search) | **GET** /v1/google/shorts/search | Google Shorts search |
| [**google_google_web_search**](GoogleApi.md#google_google_web_search) | **GET** /v1/google/search | Google web search |
| [**google_hotel_details**](GoogleApi.md#google_hotel_details) | **GET** /v1/google/hotels/details | Hotel details |
| [**google_immersive_product_detail**](GoogleApi.md#google_immersive_product_detail) | **GET** /v1/google/products/detail | Immersive product detail |
| [**google_interest_by_region**](GoogleApi.md#google_interest_by_region) | **GET** /v1/google/trends/regions | Interest by region |
| [**google_interest_over_time**](GoogleApi.md#google_interest_over_time) | **GET** /v1/google/trends/interest | Interest over time |
| [**google_multi_seller_offers_by_barcode**](GoogleApi.md#google_multi_seller_offers_by_barcode) | **GET** /v1/google/shopping/offers | Multi-seller offers by barcode |
| [**google_news_by_topic**](GoogleApi.md#google_news_by_topic) | **GET** /v1/google/news/topics | News by topic |
| [**google_patent_details**](GoogleApi.md#google_patent_details) | **GET** /v1/google/patents/detail | Patent details |
| [**google_related_topics_queries**](GoogleApi.md#google_related_topics_queries) | **GET** /v1/google/trends/related | Related topics &amp; queries |
| [**google_search_google_images**](GoogleApi.md#google_search_google_images) | **GET** /v1/google/images/search | Search Google Images |
| [**google_search_google_jobs**](GoogleApi.md#google_search_google_jobs) | **GET** /v1/google/jobs/search | Search Google Jobs |
| [**google_search_google_maps_places**](GoogleApi.md#google_search_google_maps_places) | **GET** /v1/google/maps/search | Search Google Maps places |
| [**google_search_google_news**](GoogleApi.md#google_search_google_news) | **GET** /v1/google/news/search | Search Google News |
| [**google_search_google_scholar**](GoogleApi.md#google_search_google_scholar) | **GET** /v1/google/scholar/search | Search Google Scholar |
| [**google_search_google_videos**](GoogleApi.md#google_search_google_videos) | **GET** /v1/google/videos/search | Search Google Videos |
| [**google_search_hotels**](GoogleApi.md#google_search_hotels) | **GET** /v1/google/hotels/search | Search hotels |
| [**google_search_patents**](GoogleApi.md#google_search_patents) | **GET** /v1/google/patents/search | Search patents |
| [**google_search_products**](GoogleApi.md#google_search_products) | **GET** /v1/google/shopping/search | Search products |
| [**google_search_scholar_author_profiles**](GoogleApi.md#google_search_scholar_author_profiles) | **GET** /v1/google/scholar/profiles | Search Scholar author profiles |
| [**google_trending_news**](GoogleApi.md#google_trending_news) | **GET** /v1/google/news/trending | Trending news |
| [**google_trending_searches**](GoogleApi.md#google_trending_searches) | **GET** /v1/google/trends/trending | Trending searches |
| [**google_trends_topic_autocomplete**](GoogleApi.md#google_trends_topic_autocomplete) | **GET** /v1/google/trends/autocomplete | Trends topic autocomplete |


## google_get_author_citations_per_year_chart

> Object google_get_author_citations_per_year_chart(author_id, opts)

Get author citations-per-year chart

Return the citations-per-year chart for a Google Scholar author.

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

api_instance = ScrapeBadger::GoogleApi.new
author_id = 'author_id_example' # String | Scholar user ID
opts = {
  hl: 'hl_example' # String | Language code
}

begin
  # Get author citations-per-year chart
  result = api_instance.google_get_author_citations_per_year_chart(author_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_author_citations_per_year_chart: #{e}"
end
```

#### Using the google_get_author_citations_per_year_chart_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_get_author_citations_per_year_chart_with_http_info(author_id, opts)

```ruby
begin
  # Get author citations-per-year chart
  data, status_code, headers = api_instance.google_get_author_citations_per_year_chart_with_http_info(author_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_author_citations_per_year_chart_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **author_id** | **String** | Scholar user ID |  |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_get_business_posts

> Object google_get_business_posts(data_id, opts)

Get business posts

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

api_instance = ScrapeBadger::GoogleApi.new
data_id = 'data_id_example' # String | Maps data ID
opts = {
  next_page_token: 'next_page_token_example' # String | 
}

begin
  # Get business posts
  result = api_instance.google_get_business_posts(data_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_business_posts: #{e}"
end
```

#### Using the google_get_business_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_get_business_posts_with_http_info(data_id, opts)

```ruby
begin
  # Get business posts
  data, status_code, headers = api_instance.google_get_business_posts_with_http_info(data_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_business_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data_id** | **String** | Maps data ID |  |
| **next_page_token** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_get_citation_formats_for_a_scholar_paper

> Object google_get_citation_formats_for_a_scholar_paper(q, opts)

Get citation formats for a Scholar paper

Return MLA, APA, Chicago, Harvard, and Vancouver citation formats for a paper.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Cluster ID from a search result
opts = {
  hl: 'hl_example' # String | Language code
}

begin
  # Get citation formats for a Scholar paper
  result = api_instance.google_get_citation_formats_for_a_scholar_paper(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_citation_formats_for_a_scholar_paper: #{e}"
end
```

#### Using the google_get_citation_formats_for_a_scholar_paper_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_get_citation_formats_for_a_scholar_paper_with_http_info(q, opts)

```ruby
begin
  # Get citation formats for a Scholar paper
  data, status_code, headers = api_instance.google_get_citation_formats_for_a_scholar_paper_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_citation_formats_for_a_scholar_paper_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Cluster ID from a search result |  |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_get_place_details

> Object google_get_place_details(opts)

Get place details

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

api_instance = ScrapeBadger::GoogleApi.new
opts = {
  place_id: 'place_id_example', # String | 
  data_id: 'data_id_example', # String | 
  hl: 'hl_example', # String | 
  gl: 'gl_example' # String | 
}

begin
  # Get place details
  result = api_instance.google_get_place_details(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_place_details: #{e}"
end
```

#### Using the google_get_place_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_get_place_details_with_http_info(opts)

```ruby
begin
  # Get place details
  data, status_code, headers = api_instance.google_get_place_details_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_place_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **place_id** | **String** |  | [optional] |
| **data_id** | **String** |  | [optional] |
| **hl** | **String** |  | [optional][default to &#39;en&#39;] |
| **gl** | **String** |  | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_get_place_photos

> Object google_get_place_photos(data_id, opts)

Get place photos

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

api_instance = ScrapeBadger::GoogleApi.new
data_id = 'data_id_example' # String | Maps data ID
opts = {
  hl: 'hl_example', # String | 
  next_page_token: 'next_page_token_example' # String | 
}

begin
  # Get place photos
  result = api_instance.google_get_place_photos(data_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_place_photos: #{e}"
end
```

#### Using the google_get_place_photos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_get_place_photos_with_http_info(data_id, opts)

```ruby
begin
  # Get place photos
  data, status_code, headers = api_instance.google_get_place_photos_with_http_info(data_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_place_photos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data_id** | **String** | Maps data ID |  |
| **hl** | **String** |  | [optional][default to &#39;en&#39;] |
| **next_page_token** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_get_place_reviews

> Object google_get_place_reviews(data_id, opts)

Get place reviews

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

api_instance = ScrapeBadger::GoogleApi.new
data_id = 'data_id_example' # String | Maps data ID
opts = {
  sort_by: 'sort_by_example', # String | 
  hl: 'hl_example', # String | 
  next_page_token: 'next_page_token_example', # String | 
  results: 56 # Integer | 
}

begin
  # Get place reviews
  result = api_instance.google_get_place_reviews(data_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_place_reviews: #{e}"
end
```

#### Using the google_get_place_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_get_place_reviews_with_http_info(data_id, opts)

```ruby
begin
  # Get place reviews
  data, status_code, headers = api_instance.google_get_place_reviews_with_http_info(data_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_place_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data_id** | **String** | Maps data ID |  |
| **sort_by** | **String** |  | [optional][default to &#39;qualityScore&#39;] |
| **hl** | **String** |  | [optional][default to &#39;en&#39;] |
| **next_page_token** | **String** |  | [optional] |
| **results** | **Integer** |  | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_get_scholar_author_profile

> Object google_get_scholar_author_profile(author_id, opts)

Get Scholar author profile

Get detailed Google Scholar author profile including articles, stats, co-authors.

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

api_instance = ScrapeBadger::GoogleApi.new
author_id = 'author_id_example' # String | Scholar user ID (the `user` query parameter)
opts = {
  hl: 'hl_example', # String | Language code
  cstart: 56, # Integer | Articles pagination offset
  pagesize: 56 # Integer | Articles per page
}

begin
  # Get Scholar author profile
  result = api_instance.google_get_scholar_author_profile(author_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_scholar_author_profile: #{e}"
end
```

#### Using the google_get_scholar_author_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_get_scholar_author_profile_with_http_info(author_id, opts)

```ruby
begin
  # Get Scholar author profile
  data, status_code, headers = api_instance.google_get_scholar_author_profile_with_http_info(author_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_scholar_author_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **author_id** | **String** | Scholar user ID (the &#x60;user&#x60; query parameter) |  |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **cstart** | **Integer** | Articles pagination offset | [optional][default to 0] |
| **pagesize** | **Integer** | Articles per page | [optional][default to 20] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_get_stock_index_quote

> Object google_get_stock_index_quote(q, opts)

Get stock/index quote

Get a stock or index quote from Google Finance.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Ticker and exchange (e.g. \"AAPL:NASDAQ\", \"BTC-USD\")
opts = {
  hl: 'hl_example' # String | Language code
}

begin
  # Get stock/index quote
  result = api_instance.google_get_stock_index_quote(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_stock_index_quote: #{e}"
end
```

#### Using the google_get_stock_index_quote_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_get_stock_index_quote_with_http_info(q, opts)

```ruby
begin
  # Get stock/index quote
  data, status_code, headers = api_instance.google_get_stock_index_quote_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_get_stock_index_quote_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Ticker and exchange (e.g. \&quot;AAPL:NASDAQ\&quot;, \&quot;BTC-USD\&quot;) |  |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_google_ai_mode_search

> Object google_google_ai_mode_search(q, opts)

Google AI Mode search

Get AI-generated search results from Google AI Mode.  Returns the structured `text_blocks` (paragraphs, headings, comparison `table` blocks and lists), a flat `references` source list, a compact `markdown` rendering of the whole answer and — unless `include_html` is false — the raw `answer_html` body.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search query for AI-generated response
opts = {
  gl: 'gl_example', # String | Country code
  hl: 'hl_example', # String | Language code
  include_html: true # Boolean | Include the raw `answer_html` (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured `text_blocks` + `markdown`.
}

begin
  # Google AI Mode search
  result = api_instance.google_google_ai_mode_search(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_ai_mode_search: #{e}"
end
```

#### Using the google_google_ai_mode_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_ai_mode_search_with_http_info(q, opts)

```ruby
begin
  # Google AI Mode search
  data, status_code, headers = api_instance.google_google_ai_mode_search_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_ai_mode_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query for AI-generated response |  |
| **gl** | **String** | Country code | [optional][default to &#39;us&#39;] |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **include_html** | **Boolean** | Include the raw &#x60;answer_html&#x60; (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured &#x60;text_blocks&#x60; + &#x60;markdown&#x60;. | [optional][default to true] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_google_ai_overview_inline_serp_block

> Object google_google_ai_overview_inline_serp_block(q, opts)

Google AI Overview (inline SERP block)

Get the AI Overview block Google renders inline at the top of a SERP.  Deferred overviews (where Google lazy-loads the block via a follow-up ``page_token``) are chased automatically.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search query — same shape as a Google Search query
opts = {
  gl: 'gl_example', # String | Country code
  hl: 'hl_example' # String | Language code
}

begin
  # Google AI Overview (inline SERP block)
  result = api_instance.google_google_ai_overview_inline_serp_block(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_ai_overview_inline_serp_block: #{e}"
end
```

#### Using the google_google_ai_overview_inline_serp_block_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_ai_overview_inline_serp_block_with_http_info(q, opts)

```ruby
begin
  # Google AI Overview (inline SERP block)
  data, status_code, headers = api_instance.google_google_ai_overview_inline_serp_block_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_ai_overview_inline_serp_block_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query — same shape as a Google Search query |  |
| **gl** | **String** | Country code | [optional][default to &#39;us&#39;] |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_google_flights_calendar_cheapest_fare_per_date

> Object google_google_flights_calendar_cheapest_fare_per_date(departure_id, arrival_id, outbound_date_from, outbound_date_to, opts)

Google Flights calendar — cheapest fare per date

Price a whole range of dates in one call — up to 200 dates per request.  Google Flights' own price graph / date grid: the cheapest fare per departure date instead of one search per date. Prices match `/flights/search` exactly.

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

api_instance = ScrapeBadger::GoogleApi.new
departure_id = 'departure_id_example' # String | Departure airport IATA code or location ID
arrival_id = 'arrival_id_example' # String | Arrival airport IATA code or location ID
outbound_date_from = 'outbound_date_from_example' # String | First outbound date to price (YYYY-MM-DD)
outbound_date_to = 'outbound_date_to_example' # String | Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode.
opts = {
  trip_type: 'trip_type_example', # String | one_way | round_trip
  trip_length_days: 56, # Integer | Round-trip stay length in nights (price-graph mode). Defaults to 7.
  return_date_from: 'return_date_from_example', # String | Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only.
  return_date_to: 'return_date_to_example', # String | Date-grid mode: last return date
  adults: 56, # Integer | 
  children: 56, # Integer | 
  infants_in_seat: 56, # Integer | 
  infants_on_lap: 56, # Integer | 
  travel_class: 'travel_class_example', # String | 
  currency: 'currency_example', # String | ISO-4217 currency
  gl: 'gl_example', # String | 
  hl: 'hl_example' # String | 
}

begin
  # Google Flights calendar — cheapest fare per date
  result = api_instance.google_google_flights_calendar_cheapest_fare_per_date(departure_id, arrival_id, outbound_date_from, outbound_date_to, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_flights_calendar_cheapest_fare_per_date: #{e}"
end
```

#### Using the google_google_flights_calendar_cheapest_fare_per_date_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_flights_calendar_cheapest_fare_per_date_with_http_info(departure_id, arrival_id, outbound_date_from, outbound_date_to, opts)

```ruby
begin
  # Google Flights calendar — cheapest fare per date
  data, status_code, headers = api_instance.google_google_flights_calendar_cheapest_fare_per_date_with_http_info(departure_id, arrival_id, outbound_date_from, outbound_date_to, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_flights_calendar_cheapest_fare_per_date_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **departure_id** | **String** | Departure airport IATA code or location ID |  |
| **arrival_id** | **String** | Arrival airport IATA code or location ID |  |
| **outbound_date_from** | **String** | First outbound date to price (YYYY-MM-DD) |  |
| **outbound_date_to** | **String** | Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode. |  |
| **trip_type** | **String** | one_way | round_trip | [optional][default to &#39;one_way&#39;] |
| **trip_length_days** | **Integer** | Round-trip stay length in nights (price-graph mode). Defaults to 7. | [optional] |
| **return_date_from** | **String** | Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only. | [optional] |
| **return_date_to** | **String** | Date-grid mode: last return date | [optional] |
| **adults** | **Integer** |  | [optional][default to 1] |
| **children** | **Integer** |  | [optional][default to 0] |
| **infants_in_seat** | **Integer** |  | [optional][default to 0] |
| **infants_on_lap** | **Integer** |  | [optional][default to 0] |
| **travel_class** | **String** |  | [optional][default to &#39;economy&#39;] |
| **currency** | **String** | ISO-4217 currency | [optional][default to &#39;USD&#39;] |
| **gl** | **String** |  | [optional][default to &#39;us&#39;] |
| **hl** | **String** |  | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_google_flights_search

> Object google_google_flights_search(departure_id, arrival_id, outbound_date, opts)

Google Flights search

Search Google Flights for available itineraries.

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

api_instance = ScrapeBadger::GoogleApi.new
departure_id = 'departure_id_example' # String | Departure airport IATA code or location ID
arrival_id = 'arrival_id_example' # String | Arrival airport IATA code or location ID
outbound_date = 'outbound_date_example' # String | Outbound date (YYYY-MM-DD)
opts = {
  return_date: 'return_date_example', # String | Return date (round-trip only)
  trip_type: 'trip_type_example', # String | round_trip | one_way | multi_city
  adults: 56, # Integer | 
  children: 56, # Integer | 
  infants_in_seat: 56, # Integer | 
  infants_on_lap: 56, # Integer | 
  travel_class: 'travel_class_example', # String | 
  currency: 'currency_example', # String | ISO-4217 currency
  gl: 'gl_example', # String | 
  hl: 'hl_example', # String | 
  stops: 'stops_example', # String | 
  max_price: 56, # Integer | 
  departure_token: 'departure_token_example' # String | A round-trip offer's departure_token; returns the return-leg flights for that selected outbound (round-trip only).
}

begin
  # Google Flights search
  result = api_instance.google_google_flights_search(departure_id, arrival_id, outbound_date, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_flights_search: #{e}"
end
```

#### Using the google_google_flights_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_flights_search_with_http_info(departure_id, arrival_id, outbound_date, opts)

```ruby
begin
  # Google Flights search
  data, status_code, headers = api_instance.google_google_flights_search_with_http_info(departure_id, arrival_id, outbound_date, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_flights_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **departure_id** | **String** | Departure airport IATA code or location ID |  |
| **arrival_id** | **String** | Arrival airport IATA code or location ID |  |
| **outbound_date** | **String** | Outbound date (YYYY-MM-DD) |  |
| **return_date** | **String** | Return date (round-trip only) | [optional] |
| **trip_type** | **String** | round_trip | one_way | multi_city | [optional][default to &#39;round_trip&#39;] |
| **adults** | **Integer** |  | [optional][default to 1] |
| **children** | **Integer** |  | [optional][default to 0] |
| **infants_in_seat** | **Integer** |  | [optional][default to 0] |
| **infants_on_lap** | **Integer** |  | [optional][default to 0] |
| **travel_class** | **String** |  | [optional][default to &#39;economy&#39;] |
| **currency** | **String** | ISO-4217 currency | [optional][default to &#39;USD&#39;] |
| **gl** | **String** |  | [optional][default to &#39;us&#39;] |
| **hl** | **String** |  | [optional][default to &#39;en&#39;] |
| **stops** | **String** |  | [optional][default to &#39;any&#39;] |
| **max_price** | **Integer** |  | [optional] |
| **departure_token** | **String** | A round-trip offer&#39;s departure_token; returns the return-leg flights for that selected outbound (round-trip only). | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_google_lens_visual_search

> Object google_google_lens_visual_search(url, opts)

Google Lens visual search

Google Lens visual search.  Response carries ``lens_results`` (Scrapingdog parity alias) with ``title`` / ``source`` / ``source_favicon`` / ``thumbnail`` / ``original_thumbnail`` / ``rating`` / ``reviews`` / ``in_stock``, plus ``price`` (``{value, currency, extracted}``) and the raw ``tag`` chip it is parsed from, on shoppable matches. ``related_searches`` chips come alongside. Legacy ``results`` alias kept for backwards compat.

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

api_instance = ScrapeBadger::GoogleApi.new
url = 'url_example' # String | Public URL of the image to search visually
opts = {
  query: 'query_example', # String | Optional text refinement (e.g. 'pizza')
  country: 'country_example', # String | ISO country code (alias for gl)
  language: 'language_example', # String | Language code (alias for hl)
  gl: 'gl_example', # String | Country code
  hl: 'hl_example', # String | Language code
  product: true, # Boolean | Bias towards shoppable product matches
  visual_matches: true, # Boolean | Include the visual-matches carousel
  exact_matches: true # Boolean | Restrict to exact-match results
}

begin
  # Google Lens visual search
  result = api_instance.google_google_lens_visual_search(url, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_lens_visual_search: #{e}"
end
```

#### Using the google_google_lens_visual_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_lens_visual_search_with_http_info(url, opts)

```ruby
begin
  # Google Lens visual search
  data, status_code, headers = api_instance.google_google_lens_visual_search_with_http_info(url, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_lens_visual_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Public URL of the image to search visually |  |
| **query** | **String** | Optional text refinement (e.g. &#39;pizza&#39;) | [optional] |
| **country** | **String** | ISO country code (alias for gl) | [optional] |
| **language** | **String** | Language code (alias for hl) | [optional] |
| **gl** | **String** | Country code | [optional][default to &#39;us&#39;] |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **product** | **Boolean** | Bias towards shoppable product matches | [optional][default to false] |
| **visual_matches** | **Boolean** | Include the visual-matches carousel | [optional][default to true] |
| **exact_matches** | **Boolean** | Restrict to exact-match results | [optional][default to false] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_google_scraper_health_check

> Object google_google_scraper_health_check

Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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

api_instance = ScrapeBadger::GoogleApi.new

begin
  # Google scraper health check
  result = api_instance.google_google_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_scraper_health_check: #{e}"
end
```

#### Using the google_google_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_scraper_health_check_with_http_info

```ruby
begin
  # Google scraper health check
  data, status_code, headers = api_instance.google_google_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_scraper_health_check_with_http_info: #{e}"
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


## google_google_scraper_health_check_head

> Object google_google_scraper_health_check_head

Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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

api_instance = ScrapeBadger::GoogleApi.new

begin
  # Google scraper health check
  result = api_instance.google_google_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_scraper_health_check_head: #{e}"
end
```

#### Using the google_google_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_scraper_health_check_head_with_http_info

```ruby
begin
  # Google scraper health check
  data, status_code, headers = api_instance.google_google_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_scraper_health_check_head_with_http_info: #{e}"
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


## google_google_search_suggestions

> Object google_google_search_suggestions(q, opts)

Google search suggestions

Get Google search autocomplete suggestions.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search query to get suggestions for
opts = {
  hl: 'hl_example', # String | Language code
  gl: 'gl_example' # String | Country code
}

begin
  # Google search suggestions
  result = api_instance.google_google_search_suggestions(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_search_suggestions: #{e}"
end
```

#### Using the google_google_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_search_suggestions_with_http_info(q, opts)

```ruby
begin
  # Google search suggestions
  data, status_code, headers = api_instance.google_google_search_suggestions_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query to get suggestions for |  |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **gl** | **String** | Country code | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_google_shorts_search

> Object google_google_shorts_search(q, opts)

Google Shorts search

Return short-form video results (YouTube Shorts, TikToks) from Google Shorts mode.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search query
opts = {
  gl: 'gl_example', # String | Country code
  hl: 'hl_example', # String | Language code
  domain: 'domain_example', # String | Google domain
  num: 56, # Integer | Results per page
  start: 56 # Integer | Pagination offset
}

begin
  # Google Shorts search
  result = api_instance.google_google_shorts_search(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_shorts_search: #{e}"
end
```

#### Using the google_google_shorts_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_shorts_search_with_http_info(q, opts)

```ruby
begin
  # Google Shorts search
  data, status_code, headers = api_instance.google_google_shorts_search_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_shorts_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query |  |
| **gl** | **String** | Country code | [optional][default to &#39;us&#39;] |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **domain** | **String** | Google domain | [optional][default to &#39;google.com&#39;] |
| **num** | **Integer** | Results per page | [optional][default to 20] |
| **start** | **Integer** | Pagination offset | [optional][default to 0] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_google_web_search

> Object google_google_web_search(q, opts)

Google web search

Search Google and get structured results (organic, ads, KG, AI overview, PAA).

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search query (supports Google operators)
opts = {
  gl: 'gl_example', # String | Country code
  hl: 'hl_example', # String | Language code
  num: 56, # Integer | 
  start: 56, # Integer | Page offset (0, 10, 20...)
  domain: 'domain_example', # String | Google domain
  device: 'desktop', # String | Device target: desktop, mobile, iphone, android, tablet
  user_agent: 'user_agent_example', # String | Custom User-Agent (overrides device)
  output: 'json', # String | Response format: json (parsed) or html (raw SERP)
  location: 'location_example', # String | City-level geo-targeting
  lr: 'lr_example', # String | Language restrict (e.g. lang_en)
  tbs: 'tbs_example', # String | Time filter (e.g. qdr:d)
  safe: 'safe_example', # String | 
  uule: 'uule_example', # String | UULE encoded location
  filter: 56, # Integer | Show omitted results
  nfpr: 56, # Integer | Disable auto-correction
  cr: 'cr_example', # String | Country restrict
  ludocid: 'ludocid_example', # String | Google Place CID
  lsig: 'lsig_example', # String | Knowledge Graph map ID
  kgmid: 'kgmid_example', # String | Knowledge Graph entity ID
  si: 'si_example', # String | Cached search params
  ibp: 'ibp_example', # String | Layout control
  uds: 'uds_example', # String | Google filter string
  ai_overview: true # Boolean | Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview.
}

begin
  # Google web search
  result = api_instance.google_google_web_search(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_web_search: #{e}"
end
```

#### Using the google_google_web_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_google_web_search_with_http_info(q, opts)

```ruby
begin
  # Google web search
  data, status_code, headers = api_instance.google_google_web_search_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_google_web_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query (supports Google operators) |  |
| **gl** | **String** | Country code | [optional][default to &#39;us&#39;] |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **num** | **Integer** |  | [optional][default to 10] |
| **start** | **Integer** | Page offset (0, 10, 20...) | [optional][default to 0] |
| **domain** | **String** | Google domain | [optional][default to &#39;google.com&#39;] |
| **device** | **String** | Device target: desktop, mobile, iphone, android, tablet | [optional][default to &#39;desktop&#39;] |
| **user_agent** | **String** | Custom User-Agent (overrides device) | [optional] |
| **output** | **String** | Response format: json (parsed) or html (raw SERP) | [optional][default to &#39;json&#39;] |
| **location** | **String** | City-level geo-targeting | [optional] |
| **lr** | **String** | Language restrict (e.g. lang_en) | [optional] |
| **tbs** | **String** | Time filter (e.g. qdr:d) | [optional] |
| **safe** | **String** |  | [optional][default to &#39;off&#39;] |
| **uule** | **String** | UULE encoded location | [optional] |
| **filter** | **Integer** | Show omitted results | [optional] |
| **nfpr** | **Integer** | Disable auto-correction | [optional][default to 0] |
| **cr** | **String** | Country restrict | [optional] |
| **ludocid** | **String** | Google Place CID | [optional] |
| **lsig** | **String** | Knowledge Graph map ID | [optional] |
| **kgmid** | **String** | Knowledge Graph entity ID | [optional] |
| **si** | **String** | Cached search params | [optional] |
| **ibp** | **String** | Layout control | [optional] |
| **uds** | **String** | Google filter string | [optional] |
| **ai_overview** | **Boolean** | Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview. | [optional][default to false] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_hotel_details

> Object google_hotel_details(property_token, check_in, check_out)

Hotel details

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

api_instance = ScrapeBadger::GoogleApi.new
property_token = 'property_token_example' # String | Property token
check_in = 'check_in_example' # String | YYYY-MM-DD
check_out = 'check_out_example' # String | YYYY-MM-DD

begin
  # Hotel details
  result = api_instance.google_hotel_details(property_token, check_in, check_out)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_hotel_details: #{e}"
end
```

#### Using the google_hotel_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_hotel_details_with_http_info(property_token, check_in, check_out)

```ruby
begin
  # Hotel details
  data, status_code, headers = api_instance.google_hotel_details_with_http_info(property_token, check_in, check_out)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_hotel_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **property_token** | **String** | Property token |  |
| **check_in** | **String** | YYYY-MM-DD |  |
| **check_out** | **String** | YYYY-MM-DD |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_immersive_product_detail

> Object google_immersive_product_detail(product_id, q, opts)

Immersive product detail

Get deep product details from Google's immersive product page.

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

api_instance = ScrapeBadger::GoogleApi.new
product_id = 'product_id_example' # String | Google Shopping ``gpcid`` — the product_id returned on ``/shopping/search`` tiles. Scrapingdog-compatible.
q = 'q_example' # String | Original search query that surfaced the product. Required by Google's ``/async/oapv`` RPC.
opts = {
  gl: 'gl_example', # String | Country code (ISO 3166 alpha-2)
  hl: 'hl_example', # String | Language code
  catalog_id: 'catalog_id_example', # String | Optional ``catalogid`` from the Shopping tile (improves parity).
  image_docid: 'image_docid_example', # String | Optional ``imageDocid`` for higher-fidelity images.
  headline_offer_docid: 'headline_offer_docid_example', # String | Optional ``headlineOfferDocid`` to pin the featured seller.
  mid: 'mid_example', # String | Optional Google Knowledge-Graph ``mid``.
  include_offers: true, # Boolean | When true, fetch the full merchant-offer list via a secondary RPC (``/async/piu_ps``). Adds ~1 s.
  include_variants: true # Boolean | When true, fetch size/colour variants via a secondary RPC (``/async/toy_v``). Adds ~1 s.
}

begin
  # Immersive product detail
  result = api_instance.google_immersive_product_detail(product_id, q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_immersive_product_detail: #{e}"
end
```

#### Using the google_immersive_product_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_immersive_product_detail_with_http_info(product_id, q, opts)

```ruby
begin
  # Immersive product detail
  data, status_code, headers = api_instance.google_immersive_product_detail_with_http_info(product_id, q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_immersive_product_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | Google Shopping &#x60;&#x60;gpcid&#x60;&#x60; — the product_id returned on &#x60;&#x60;/shopping/search&#x60;&#x60; tiles. Scrapingdog-compatible. |  |
| **q** | **String** | Original search query that surfaced the product. Required by Google&#39;s &#x60;&#x60;/async/oapv&#x60;&#x60; RPC. |  |
| **gl** | **String** | Country code (ISO 3166 alpha-2) | [optional][default to &#39;us&#39;] |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **catalog_id** | **String** | Optional &#x60;&#x60;catalogid&#x60;&#x60; from the Shopping tile (improves parity). | [optional] |
| **image_docid** | **String** | Optional &#x60;&#x60;imageDocid&#x60;&#x60; for higher-fidelity images. | [optional] |
| **headline_offer_docid** | **String** | Optional &#x60;&#x60;headlineOfferDocid&#x60;&#x60; to pin the featured seller. | [optional] |
| **mid** | **String** | Optional Google Knowledge-Graph &#x60;&#x60;mid&#x60;&#x60;. | [optional] |
| **include_offers** | **Boolean** | When true, fetch the full merchant-offer list via a secondary RPC (&#x60;&#x60;/async/piu_ps&#x60;&#x60;). Adds ~1 s. | [optional][default to false] |
| **include_variants** | **Boolean** | When true, fetch size/colour variants via a secondary RPC (&#x60;&#x60;/async/toy_v&#x60;&#x60;). Adds ~1 s. | [optional][default to false] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_interest_by_region

> Object google_interest_by_region(q, opts)

Interest by region

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search term
opts = {
  geo: 'geo_example' # String | 
}

begin
  # Interest by region
  result = api_instance.google_interest_by_region(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_interest_by_region: #{e}"
end
```

#### Using the google_interest_by_region_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_interest_by_region_with_http_info(q, opts)

```ruby
begin
  # Interest by region
  data, status_code, headers = api_instance.google_interest_by_region_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_interest_by_region_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search term |  |
| **geo** | **String** |  | [optional][default to &#39;&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_interest_over_time

> Object google_interest_over_time(q, opts)

Interest over time

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search terms
opts = {
  geo: 'geo_example', # String | 
  date: 'date_example' # String | 
}

begin
  # Interest over time
  result = api_instance.google_interest_over_time(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_interest_over_time: #{e}"
end
```

#### Using the google_interest_over_time_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_interest_over_time_with_http_info(q, opts)

```ruby
begin
  # Interest over time
  data, status_code, headers = api_instance.google_interest_over_time_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_interest_over_time_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search terms |  |
| **geo** | **String** |  | [optional][default to &#39;&#39;] |
| **date** | **String** |  | [optional][default to &#39;today 12-m&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_multi_seller_offers_by_barcode

> Object google_multi_seller_offers_by_barcode(barcode, opts)

Multi-seller offers by barcode

Resolve a barcode to a product via Google web search, then return its Google Shopping seller offers (source + price per merchant).

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

api_instance = ScrapeBadger::GoogleApi.new
barcode = 'barcode_example' # String | Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14
opts = {
  gl: 'gl_example', # String | Country code (ISO 3166 alpha-2)
  hl: 'hl_example' # String | Language code
}

begin
  # Multi-seller offers by barcode
  result = api_instance.google_multi_seller_offers_by_barcode(barcode, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_multi_seller_offers_by_barcode: #{e}"
end
```

#### Using the google_multi_seller_offers_by_barcode_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_multi_seller_offers_by_barcode_with_http_info(barcode, opts)

```ruby
begin
  # Multi-seller offers by barcode
  data, status_code, headers = api_instance.google_multi_seller_offers_by_barcode_with_http_info(barcode, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_multi_seller_offers_by_barcode_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **barcode** | **String** | Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14 |  |
| **gl** | **String** | Country code (ISO 3166 alpha-2) | [optional] |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_news_by_topic

> Object google_news_by_topic(topic, opts)

News by topic

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

api_instance = ScrapeBadger::GoogleApi.new
topic = 'topic_example' # String | Topic name
opts = {
  hl: 'hl_example', # String | 
  gl: 'gl_example', # String | 
  max_results: 56 # Integer | 
}

begin
  # News by topic
  result = api_instance.google_news_by_topic(topic, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_news_by_topic: #{e}"
end
```

#### Using the google_news_by_topic_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_news_by_topic_with_http_info(topic, opts)

```ruby
begin
  # News by topic
  data, status_code, headers = api_instance.google_news_by_topic_with_http_info(topic, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_news_by_topic_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **topic** | **String** | Topic name |  |
| **hl** | **String** |  | [optional][default to &#39;en&#39;] |
| **gl** | **String** |  | [optional][default to &#39;US&#39;] |
| **max_results** | **Integer** |  | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_patent_details

> Object google_patent_details(patent_id)

Patent details

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

api_instance = ScrapeBadger::GoogleApi.new
patent_id = 'patent_id_example' # String | Patent number

begin
  # Patent details
  result = api_instance.google_patent_details(patent_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_patent_details: #{e}"
end
```

#### Using the google_patent_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_patent_details_with_http_info(patent_id)

```ruby
begin
  # Patent details
  data, status_code, headers = api_instance.google_patent_details_with_http_info(patent_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_patent_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **patent_id** | **String** | Patent number |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_related_topics_queries

> Object google_related_topics_queries(q, opts)

Related topics & queries

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search term
opts = {
  geo: 'geo_example' # String | 
}

begin
  # Related topics & queries
  result = api_instance.google_related_topics_queries(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_related_topics_queries: #{e}"
end
```

#### Using the google_related_topics_queries_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_related_topics_queries_with_http_info(q, opts)

```ruby
begin
  # Related topics & queries
  data, status_code, headers = api_instance.google_related_topics_queries_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_related_topics_queries_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search term |  |
| **geo** | **String** |  | [optional][default to &#39;&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_google_images

> Object google_search_google_images(q, opts)

Search Google Images

Search Google Images for visual content.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Image search query
opts = {
  gl: 'gl_example', # String | Country code
  hl: 'hl_example', # String | Language code
  tbs: 'tbs_example', # String | Time/filter string (e.g. qdr:d)
  imgsz: 'imgsz_example', # String | Image size: l, m, i, xXl
  imgcolor: 'imgcolor_example', # String | Image color filter
  imgtype: 'imgtype_example', # String | Image type: face, photo, clipart
  safe: 'safe_example', # String | Safe search
  page: 56 # Integer | Page number
}

begin
  # Search Google Images
  result = api_instance.google_search_google_images(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_images: #{e}"
end
```

#### Using the google_search_google_images_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_google_images_with_http_info(q, opts)

```ruby
begin
  # Search Google Images
  data, status_code, headers = api_instance.google_search_google_images_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_images_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Image search query |  |
| **gl** | **String** | Country code | [optional][default to &#39;us&#39;] |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **tbs** | **String** | Time/filter string (e.g. qdr:d) | [optional] |
| **imgsz** | **String** | Image size: l, m, i, xXl | [optional] |
| **imgcolor** | **String** | Image color filter | [optional] |
| **imgtype** | **String** | Image type: face, photo, clipart | [optional] |
| **safe** | **String** | Safe search | [optional][default to &#39;off&#39;] |
| **page** | **Integer** | Page number | [optional][default to 0] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_google_jobs

> Object google_search_google_jobs(q, opts)

Search Google Jobs

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Job title, keywords
opts = {
  location: 'location_example', # String | 
  gl: 'gl_example', # String | 
  job_type: 'job_type_example', # String | 
  date_posted: 'date_posted_example' # String | 
}

begin
  # Search Google Jobs
  result = api_instance.google_search_google_jobs(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_jobs: #{e}"
end
```

#### Using the google_search_google_jobs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_google_jobs_with_http_info(q, opts)

```ruby
begin
  # Search Google Jobs
  data, status_code, headers = api_instance.google_search_google_jobs_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_jobs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Job title, keywords |  |
| **location** | **String** |  | [optional] |
| **gl** | **String** |  | [optional][default to &#39;us&#39;] |
| **job_type** | **String** |  | [optional] |
| **date_posted** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_google_maps_places

> Object google_search_google_maps_places(q, opts)

Search Google Maps places

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search query
opts = {
  ll: 'll_example', # String | 
  gl: 'gl_example', # String | 
  hl: 'hl_example', # String | 
  start: 56 # Integer | 
}

begin
  # Search Google Maps places
  result = api_instance.google_search_google_maps_places(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_maps_places: #{e}"
end
```

#### Using the google_search_google_maps_places_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_google_maps_places_with_http_info(q, opts)

```ruby
begin
  # Search Google Maps places
  data, status_code, headers = api_instance.google_search_google_maps_places_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_maps_places_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query |  |
| **ll** | **String** |  | [optional] |
| **gl** | **String** |  | [optional][default to &#39;us&#39;] |
| **hl** | **String** |  | [optional][default to &#39;en&#39;] |
| **start** | **Integer** |  | [optional][default to 0] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_google_news

> Object google_search_google_news(q, opts)

Search Google News

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search query
opts = {
  hl: 'hl_example', # String | 
  gl: 'gl_example', # String | 
  max_results: 56 # Integer | 
}

begin
  # Search Google News
  result = api_instance.google_search_google_news(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_news: #{e}"
end
```

#### Using the google_search_google_news_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_google_news_with_http_info(q, opts)

```ruby
begin
  # Search Google News
  data, status_code, headers = api_instance.google_search_google_news_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_news_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query |  |
| **hl** | **String** |  | [optional][default to &#39;en&#39;] |
| **gl** | **String** |  | [optional][default to &#39;US&#39;] |
| **max_results** | **Integer** |  | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_google_scholar

> Object google_search_google_scholar(q, opts)

Search Google Scholar

Search Google Scholar for scholarly articles.  Each result ships with its doc ``id``, ``type`` badge ([BOOK]/[PDF]/...), wrapped ``inline_links`` (versions + cited_by + related), PDF ``resources`` list, and structured ``authors`` (with ``author_id`` for profiled authors — pipe straight into ``/scholar/author``). Envelope carries ``scholar_results`` alias (Scrapingdog parity), ``related_searches``, and matched ``profiles`` cards.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search query for scholarly articles
opts = {
  hl: 'hl_example', # String | Language code
  as_ylo: 56, # Integer | Year from (e.g. 2020)
  as_yhi: 56, # Integer | Year to (e.g. 2024)
  as_sdt: 'as_sdt_example', # String | Search type: 0=exclude patents, 7=include
  page: 56, # Integer | Page number (0-based)
  num: 56 # Integer | Results per page (max 20)
}

begin
  # Search Google Scholar
  result = api_instance.google_search_google_scholar(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_scholar: #{e}"
end
```

#### Using the google_search_google_scholar_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_google_scholar_with_http_info(q, opts)

```ruby
begin
  # Search Google Scholar
  data, status_code, headers = api_instance.google_search_google_scholar_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_scholar_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query for scholarly articles |  |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **as_ylo** | **Integer** | Year from (e.g. 2020) | [optional] |
| **as_yhi** | **Integer** | Year to (e.g. 2024) | [optional] |
| **as_sdt** | **String** | Search type: 0&#x3D;exclude patents, 7&#x3D;include | [optional][default to &#39;0&#39;] |
| **page** | **Integer** | Page number (0-based) | [optional][default to 0] |
| **num** | **Integer** | Results per page (max 20) | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_google_videos

> Object google_search_google_videos(q, opts)

Search Google Videos

Search Google for video results.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Video search query
opts = {
  gl: 'gl_example', # String | Country code
  hl: 'hl_example', # String | Language code
  tbs: 'tbs_example', # String | Time filter (e.g. qdr:d)
  safe: 'safe_example', # String | Safe search
  page: 56 # Integer | Page number
}

begin
  # Search Google Videos
  result = api_instance.google_search_google_videos(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_videos: #{e}"
end
```

#### Using the google_search_google_videos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_google_videos_with_http_info(q, opts)

```ruby
begin
  # Search Google Videos
  data, status_code, headers = api_instance.google_search_google_videos_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_google_videos_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Video search query |  |
| **gl** | **String** | Country code | [optional][default to &#39;us&#39;] |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **tbs** | **String** | Time filter (e.g. qdr:d) | [optional] |
| **safe** | **String** | Safe search | [optional][default to &#39;off&#39;] |
| **page** | **Integer** | Page number | [optional][default to 0] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_hotels

> Object google_search_hotels(q, check_in, check_out, opts)

Search hotels

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Location or hotel name
check_in = 'check_in_example' # String | YYYY-MM-DD
check_out = 'check_out_example' # String | YYYY-MM-DD
opts = {
  adults: 56, # Integer | 
  currency: 'currency_example', # String | 
  gl: 'gl_example' # String | 
}

begin
  # Search hotels
  result = api_instance.google_search_hotels(q, check_in, check_out, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_hotels: #{e}"
end
```

#### Using the google_search_hotels_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_hotels_with_http_info(q, check_in, check_out, opts)

```ruby
begin
  # Search hotels
  data, status_code, headers = api_instance.google_search_hotels_with_http_info(q, check_in, check_out, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_hotels_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Location or hotel name |  |
| **check_in** | **String** | YYYY-MM-DD |  |
| **check_out** | **String** | YYYY-MM-DD |  |
| **adults** | **Integer** |  | [optional][default to 2] |
| **currency** | **String** |  | [optional][default to &#39;USD&#39;] |
| **gl** | **String** |  | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_patents

> Object google_search_patents(q, opts)

Search patents

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Search query (Boolean logic supported)
opts = {
  page: 56, # Integer | 
  num: 56, # Integer | 
  sort: 'sort_example', # String | 'new' or 'old'
  inventor: 'inventor_example', # String | Inventor name(s)
  assignee: 'assignee_example', # String | Assignee / company name(s)
  country: 'country_example', # String | Country code (US, EP, WO, …)
  language: 'language_example', # String | Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH
  status: 'status_example', # String | GRANT or APPLICATION
  patent_type: 'patent_type_example', # String | PATENT or DESIGN
  before: 'before_example', # String | Before date YYYYMMDD
  after: 'after_example' # String | After date YYYYMMDD
}

begin
  # Search patents
  result = api_instance.google_search_patents(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_patents: #{e}"
end
```

#### Using the google_search_patents_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_patents_with_http_info(q, opts)

```ruby
begin
  # Search patents
  data, status_code, headers = api_instance.google_search_patents_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_patents_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query (Boolean logic supported) |  |
| **page** | **Integer** |  | [optional][default to 0] |
| **num** | **Integer** |  | [optional][default to 10] |
| **sort** | **String** | &#39;new&#39; or &#39;old&#39; | [optional] |
| **inventor** | **String** | Inventor name(s) | [optional] |
| **assignee** | **String** | Assignee / company name(s) | [optional] |
| **country** | **String** | Country code (US, EP, WO, …) | [optional] |
| **language** | **String** | Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH | [optional] |
| **status** | **String** | GRANT or APPLICATION | [optional] |
| **patent_type** | **String** | PATENT or DESIGN | [optional] |
| **before** | **String** | Before date YYYYMMDD | [optional] |
| **after** | **String** | After date YYYYMMDD | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_products

> Object google_search_products(q, opts)

Search products

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Product search query
opts = {
  gl: 'gl_example', # String | 
  min_price: 56, # Integer | 
  max_price: 56, # Integer | 
  sort_by: 'sort_by_example' # String | 
}

begin
  # Search products
  result = api_instance.google_search_products(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_products: #{e}"
end
```

#### Using the google_search_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_products_with_http_info(q, opts)

```ruby
begin
  # Search products
  data, status_code, headers = api_instance.google_search_products_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Product search query |  |
| **gl** | **String** |  | [optional][default to &#39;us&#39;] |
| **min_price** | **Integer** |  | [optional] |
| **max_price** | **Integer** |  | [optional] |
| **sort_by** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_search_scholar_author_profiles

> Object google_search_scholar_author_profiles(mauthors, opts)

Search Scholar author profiles

Search Google Scholar for author profiles by name.

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

api_instance = ScrapeBadger::GoogleApi.new
mauthors = 'mauthors_example' # String | Author name query (e.g. 'Geoffrey Hinton')
opts = {
  hl: 'hl_example', # String | Language code
  after_author: 'after_author_example', # String | Pagination token (next page)
  before_author: 'before_author_example' # String | Pagination token (previous page)
}

begin
  # Search Scholar author profiles
  result = api_instance.google_search_scholar_author_profiles(mauthors, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_scholar_author_profiles: #{e}"
end
```

#### Using the google_search_scholar_author_profiles_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_search_scholar_author_profiles_with_http_info(mauthors, opts)

```ruby
begin
  # Search Scholar author profiles
  data, status_code, headers = api_instance.google_search_scholar_author_profiles_with_http_info(mauthors, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_search_scholar_author_profiles_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **mauthors** | **String** | Author name query (e.g. &#39;Geoffrey Hinton&#39;) |  |
| **hl** | **String** | Language code | [optional][default to &#39;en&#39;] |
| **after_author** | **String** | Pagination token (next page) | [optional] |
| **before_author** | **String** | Pagination token (previous page) | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_trending_news

> Object google_trending_news(opts)

Trending news

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

api_instance = ScrapeBadger::GoogleApi.new
opts = {
  hl: 'hl_example', # String | 
  gl: 'gl_example', # String | 
  max_results: 56 # Integer | 
}

begin
  # Trending news
  result = api_instance.google_trending_news(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_trending_news: #{e}"
end
```

#### Using the google_trending_news_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_trending_news_with_http_info(opts)

```ruby
begin
  # Trending news
  data, status_code, headers = api_instance.google_trending_news_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_trending_news_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **hl** | **String** |  | [optional][default to &#39;en&#39;] |
| **gl** | **String** |  | [optional][default to &#39;US&#39;] |
| **max_results** | **Integer** |  | [optional][default to 10] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_trending_searches

> Object google_trending_searches(opts)

Trending searches

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

api_instance = ScrapeBadger::GoogleApi.new
opts = {
  geo: 'geo_example' # String | 
}

begin
  # Trending searches
  result = api_instance.google_trending_searches(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_trending_searches: #{e}"
end
```

#### Using the google_trending_searches_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_trending_searches_with_http_info(opts)

```ruby
begin
  # Trending searches
  data, status_code, headers = api_instance.google_trending_searches_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_trending_searches_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **geo** | **String** |  | [optional][default to &#39;US&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## google_trends_topic_autocomplete

> Object google_trends_topic_autocomplete(q, opts)

Trends topic autocomplete

Return categorized Knowledge Graph topic entities (mid, type) for a query.

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

api_instance = ScrapeBadger::GoogleApi.new
q = 'q_example' # String | Query prefix to resolve into Trends topics
opts = {
  hl: 'hl_example', # String | Language code
  tz: 'tz_example' # String | Timezone offset in minutes
}

begin
  # Trends topic autocomplete
  result = api_instance.google_trends_topic_autocomplete(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_trends_topic_autocomplete: #{e}"
end
```

#### Using the google_trends_topic_autocomplete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> google_trends_topic_autocomplete_with_http_info(q, opts)

```ruby
begin
  # Trends topic autocomplete
  data, status_code, headers = api_instance.google_trends_topic_autocomplete_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GoogleApi->google_trends_topic_autocomplete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Query prefix to resolve into Trends topics |  |
| **hl** | **String** | Language code | [optional][default to &#39;en-US&#39;] |
| **tz** | **String** | Timezone offset in minutes | [optional][default to &#39;0&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

