# ScrapeBadger::LinkedInApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**linkedin_get_a_company_s_job_postings**](LinkedInApi.md#linkedin_get_a_company_s_job_postings) | **GET** /v1/linkedin/companies/{company_id}/jobs | Get a company&#39;s job postings |
| [**linkedin_get_a_course**](LinkedInApi.md#linkedin_get_a_course) | **GET** /v1/linkedin/learning/{course_slug} | Get a course |
| [**linkedin_get_a_public_article**](LinkedInApi.md#linkedin_get_a_public_article) | **GET** /v1/linkedin/articles/{article_slug} | Get a public article |
| [**linkedin_get_a_public_post**](LinkedInApi.md#linkedin_get_a_public_post) | **GET** /v1/linkedin/posts/{post_slug} | Get a public post |
| [**linkedin_get_company**](LinkedInApi.md#linkedin_get_company) | **GET** /v1/linkedin/companies/{universal_name} | Get company |
| [**linkedin_get_job_detail**](LinkedInApi.md#linkedin_get_job_detail) | **GET** /v1/linkedin/jobs/{job_id} | Get job detail |
| [**linkedin_get_public_profile**](LinkedInApi.md#linkedin_get_public_profile) | **GET** /v1/linkedin/profiles/{public_id} | Get public profile |
| [**linkedin_get_school**](LinkedInApi.md#linkedin_get_school) | **GET** /v1/linkedin/schools/{universal_name} | Get school |
| [**linkedin_linkedin_scraper_health_check**](LinkedInApi.md#linkedin_linkedin_scraper_health_check) | **GET** /v1/linkedin/health | LinkedIn scraper health check |
| [**linkedin_linkedin_scraper_health_check_head**](LinkedInApi.md#linkedin_linkedin_scraper_health_check_head) | **HEAD** /v1/linkedin/health | LinkedIn scraper health check |
| [**linkedin_search_linkedin_jobs**](LinkedInApi.md#linkedin_search_linkedin_jobs) | **GET** /v1/linkedin/jobs/search | Search LinkedIn jobs |
| [**linkedin_suggest_location_geo_ids**](LinkedInApi.md#linkedin_suggest_location_geo_ids) | **GET** /v1/linkedin/geo/suggest | Suggest location geo ids |


## linkedin_get_a_company_s_job_postings

> Object linkedin_get_a_company_s_job_postings(company_id, opts)

Get a company's job postings

Public job postings for a company (numeric company id from the company endpoint).

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

api_instance = ScrapeBadger::LinkedInApi.new
company_id = 'company_id_example' # String | 
opts = {
  start: 56, # Integer | Pagination offset (0, 25, 50, ...)
  country: 'country_example' # String | Residential proxy country
}

begin
  # Get a company's job postings
  result = api_instance.linkedin_get_a_company_s_job_postings(company_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_a_company_s_job_postings: #{e}"
end
```

#### Using the linkedin_get_a_company_s_job_postings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_get_a_company_s_job_postings_with_http_info(company_id, opts)

```ruby
begin
  # Get a company's job postings
  data, status_code, headers = api_instance.linkedin_get_a_company_s_job_postings_with_http_info(company_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_a_company_s_job_postings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_id** | **String** |  |  |
| **start** | **Integer** | Pagination offset (0, 25, 50, ...) | [optional][default to 0] |
| **country** | **String** | Residential proxy country | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## linkedin_get_a_course

> Object linkedin_get_a_course(course_slug, opts)

Get a course

A public LinkedIn Learning course — provider, workload, instructors, rating.

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

api_instance = ScrapeBadger::LinkedInApi.new
course_slug = 'course_slug_example' # String | 
opts = {
  country: 'country_example' # String | Residential proxy country
}

begin
  # Get a course
  result = api_instance.linkedin_get_a_course(course_slug, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_a_course: #{e}"
end
```

#### Using the linkedin_get_a_course_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_get_a_course_with_http_info(course_slug, opts)

```ruby
begin
  # Get a course
  data, status_code, headers = api_instance.linkedin_get_a_course_with_http_info(course_slug, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_a_course_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **course_slug** | **String** |  |  |
| **country** | **String** | Residential proxy country | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## linkedin_get_a_public_article

> Object linkedin_get_a_public_article(article_slug, opts)

Get a public article

A public Pulse article — title, body, author, reactions (JSON-LD).

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

api_instance = ScrapeBadger::LinkedInApi.new
article_slug = 'article_slug_example' # String | 
opts = {
  country: 'country_example' # String | Residential proxy country
}

begin
  # Get a public article
  result = api_instance.linkedin_get_a_public_article(article_slug, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_a_public_article: #{e}"
end
```

#### Using the linkedin_get_a_public_article_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_get_a_public_article_with_http_info(article_slug, opts)

```ruby
begin
  # Get a public article
  data, status_code, headers = api_instance.linkedin_get_a_public_article_with_http_info(article_slug, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_a_public_article_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **article_slug** | **String** |  |  |
| **country** | **String** | Residential proxy country | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## linkedin_get_a_public_post

> Object linkedin_get_a_public_post(post_slug, opts)

Get a public post

A public activity share — text, author, reactions, comments (JSON-LD).

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

api_instance = ScrapeBadger::LinkedInApi.new
post_slug = 'post_slug_example' # String | 
opts = {
  country: 'country_example' # String | Residential proxy country
}

begin
  # Get a public post
  result = api_instance.linkedin_get_a_public_post(post_slug, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_a_public_post: #{e}"
end
```

#### Using the linkedin_get_a_public_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_get_a_public_post_with_http_info(post_slug, opts)

```ruby
begin
  # Get a public post
  data, status_code, headers = api_instance.linkedin_get_a_public_post_with_http_info(post_slug, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_a_public_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_slug** | **String** |  |  |
| **country** | **String** | Residential proxy country | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## linkedin_get_company

> Object linkedin_get_company(universal_name, opts)

Get company

Public company page — industry, size, HQ, followers, specialties (JSON-LD + SSR).

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

api_instance = ScrapeBadger::LinkedInApi.new
universal_name = 'universal_name_example' # String | 
opts = {
  country: 'country_example' # String | Residential proxy country
}

begin
  # Get company
  result = api_instance.linkedin_get_company(universal_name, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_company: #{e}"
end
```

#### Using the linkedin_get_company_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_get_company_with_http_info(universal_name, opts)

```ruby
begin
  # Get company
  data, status_code, headers = api_instance.linkedin_get_company_with_http_info(universal_name, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_company_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **universal_name** | **String** |  |  |
| **country** | **String** | Residential proxy country | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## linkedin_get_job_detail

> Object linkedin_get_job_detail(job_id, opts)

Get job detail

Full detail for one job posting (guest API, no login).

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

api_instance = ScrapeBadger::LinkedInApi.new
job_id = 'job_id_example' # String | 
opts = {
  country: 'country_example' # String | Residential proxy country
}

begin
  # Get job detail
  result = api_instance.linkedin_get_job_detail(job_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_job_detail: #{e}"
end
```

#### Using the linkedin_get_job_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_get_job_detail_with_http_info(job_id, opts)

```ruby
begin
  # Get job detail
  data, status_code, headers = api_instance.linkedin_get_job_detail_with_http_info(job_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_job_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **job_id** | **String** |  |  |
| **country** | **String** | Residential proxy country | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## linkedin_get_public_profile

> Object linkedin_get_public_profile(public_id, opts)

Get public profile

Public profile by vanity id (the ``/in/{public_id}`` slug) — name, headline, location, about, experience, education (public JSON-LD + SSR subset).

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

api_instance = ScrapeBadger::LinkedInApi.new
public_id = 'public_id_example' # String | 
opts = {
  country: 'country_example' # String | Residential proxy country
}

begin
  # Get public profile
  result = api_instance.linkedin_get_public_profile(public_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_public_profile: #{e}"
end
```

#### Using the linkedin_get_public_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_get_public_profile_with_http_info(public_id, opts)

```ruby
begin
  # Get public profile
  data, status_code, headers = api_instance.linkedin_get_public_profile_with_http_info(public_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_public_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **public_id** | **String** |  |  |
| **country** | **String** | Residential proxy country | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## linkedin_get_school

> Object linkedin_get_school(universal_name, opts)

Get school

Public school page — name, description, website, follower/alumni counts.

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

api_instance = ScrapeBadger::LinkedInApi.new
universal_name = 'universal_name_example' # String | 
opts = {
  country: 'country_example' # String | Residential proxy country
}

begin
  # Get school
  result = api_instance.linkedin_get_school(universal_name, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_school: #{e}"
end
```

#### Using the linkedin_get_school_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_get_school_with_http_info(universal_name, opts)

```ruby
begin
  # Get school
  data, status_code, headers = api_instance.linkedin_get_school_with_http_info(universal_name, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_get_school_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **universal_name** | **String** |  |  |
| **country** | **String** | Residential proxy country | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## linkedin_linkedin_scraper_health_check

> Object linkedin_linkedin_scraper_health_check

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::LinkedInApi.new

begin
  # LinkedIn scraper health check
  result = api_instance.linkedin_linkedin_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_linkedin_scraper_health_check: #{e}"
end
```

#### Using the linkedin_linkedin_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_linkedin_scraper_health_check_with_http_info

```ruby
begin
  # LinkedIn scraper health check
  data, status_code, headers = api_instance.linkedin_linkedin_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_linkedin_scraper_health_check_with_http_info: #{e}"
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


## linkedin_linkedin_scraper_health_check_head

> Object linkedin_linkedin_scraper_health_check_head

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::LinkedInApi.new

begin
  # LinkedIn scraper health check
  result = api_instance.linkedin_linkedin_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_linkedin_scraper_health_check_head: #{e}"
end
```

#### Using the linkedin_linkedin_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_linkedin_scraper_health_check_head_with_http_info

```ruby
begin
  # LinkedIn scraper health check
  data, status_code, headers = api_instance.linkedin_linkedin_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_linkedin_scraper_health_check_head_with_http_info: #{e}"
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


## linkedin_search_linkedin_jobs

> Object linkedin_search_linkedin_jobs(opts)

Search LinkedIn jobs

Search public LinkedIn job postings (guest API, no login).

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

api_instance = ScrapeBadger::LinkedInApi.new
opts = {
  keywords: 'keywords_example', # String | Job title / keywords
  location: 'location_example', # String | Location text, e.g. 'New York'
  geo_id: 'geo_id_example', # String | LinkedIn numeric geo id (overrides location)
  company_id: 'company_id_example', # String | Restrict to a company (numeric id)
  date_posted: 'date_posted_example', # String | past_24h | past_week | past_month | any
  experience: 'experience_example', # String | internship|entry|associate|mid_senior|director|executive (comma-separated)
  job_type: 'job_type_example', # String | full_time|part_time|contract|temporary|internship|volunteer|other
  workplace: 'workplace_example', # String | onsite|remote|hybrid (comma-separated)
  sort: 'sort_example', # String | relevant | recent
  start: 56, # Integer | Pagination offset (0, 25, 50, ...)
  country: 'country_example' # String | Residential proxy country
}

begin
  # Search LinkedIn jobs
  result = api_instance.linkedin_search_linkedin_jobs(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_search_linkedin_jobs: #{e}"
end
```

#### Using the linkedin_search_linkedin_jobs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_search_linkedin_jobs_with_http_info(opts)

```ruby
begin
  # Search LinkedIn jobs
  data, status_code, headers = api_instance.linkedin_search_linkedin_jobs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_search_linkedin_jobs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **keywords** | **String** | Job title / keywords | [optional] |
| **location** | **String** | Location text, e.g. &#39;New York&#39; | [optional] |
| **geo_id** | **String** | LinkedIn numeric geo id (overrides location) | [optional] |
| **company_id** | **String** | Restrict to a company (numeric id) | [optional] |
| **date_posted** | **String** | past_24h | past_week | past_month | any | [optional] |
| **experience** | **String** | internship|entry|associate|mid_senior|director|executive (comma-separated) | [optional] |
| **job_type** | **String** | full_time|part_time|contract|temporary|internship|volunteer|other | [optional] |
| **workplace** | **String** | onsite|remote|hybrid (comma-separated) | [optional] |
| **sort** | **String** | relevant | recent | [optional] |
| **start** | **Integer** | Pagination offset (0, 25, 50, ...) | [optional][default to 0] |
| **country** | **String** | Residential proxy country | [optional][default to &#39;us&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## linkedin_suggest_location_geo_ids

> Object linkedin_suggest_location_geo_ids(query, opts)

Suggest location geo ids

Resolve a name to LinkedIn ids (job-search ``geo_id`` / ``company_id`` helper).

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

api_instance = ScrapeBadger::LinkedInApi.new
query = 'query_example' # String | Location text, e.g. 'London'
opts = {
  type: 'type_example' # String | geo | company
}

begin
  # Suggest location geo ids
  result = api_instance.linkedin_suggest_location_geo_ids(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_suggest_location_geo_ids: #{e}"
end
```

#### Using the linkedin_suggest_location_geo_ids_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> linkedin_suggest_location_geo_ids_with_http_info(query, opts)

```ruby
begin
  # Suggest location geo ids
  data, status_code, headers = api_instance.linkedin_suggest_location_geo_ids_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling LinkedInApi->linkedin_suggest_location_geo_ids_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Location text, e.g. &#39;London&#39; |  |
| **type** | **String** | geo | company | [optional][default to &#39;geo&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

