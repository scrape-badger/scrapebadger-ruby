# ScrapeBadger::WebApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**web_detect_anti_bot_and_captcha_systems**](WebApi.md#web_detect_anti_bot_and_captcha_systems) | **POST** /v1/web/detect | Detect anti-bot and CAPTCHA systems |
| [**web_extract_structured_data**](WebApi.md#web_extract_structured_data) | **POST** /v1/web/extract | Extract structured data |
| [**web_get_batch_job_status**](WebApi.md#web_get_batch_job_status) | **GET** /v1/web/batch/{job_id} | Get batch job status |
| [**web_poll_an_auto_unblock_discovery_job**](WebApi.md#web_poll_an_auto_unblock_discovery_job) | **GET** /v1/web/unblock/{job_id} | Poll an auto-unblock discovery job |
| [**web_scrape_a_url**](WebApi.md#web_scrape_a_url) | **POST** /v1/web/scrape | Scrape a URL |
| [**web_submit_batch_scraping_job**](WebApi.md#web_submit_batch_scraping_job) | **POST** /v1/web/batch | Submit batch scraping job |
| [**web_take_a_screenshot**](WebApi.md#web_take_a_screenshot) | **POST** /v1/web/screenshot | Take a screenshot |
| [**web_web_scraper_health_check**](WebApi.md#web_web_scraper_health_check) | **GET** /v1/web/health | Web scraper health check |
| [**web_web_scraper_health_check_head**](WebApi.md#web_web_scraper_health_check_head) | **HEAD** /v1/web/health | Web scraper health check |


## web_detect_anti_bot_and_captcha_systems

> Object web_detect_anti_bot_and_captcha_systems

Detect anti-bot and CAPTCHA systems

Detect which anti-bot and CAPTCHA systems are present on a URL.  Uses rnet to fetch the page and identify DataDome, Cloudflare, Akamai, Kasada, Amazon WAF, reCAPTCHA, hCaptcha, GeeTest, and more. Cost: 1 credit.

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

api_instance = ScrapeBadger::WebApi.new

begin
  # Detect anti-bot and CAPTCHA systems
  result = api_instance.web_detect_anti_bot_and_captcha_systems
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_detect_anti_bot_and_captcha_systems: #{e}"
end
```

#### Using the web_detect_anti_bot_and_captcha_systems_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> web_detect_anti_bot_and_captcha_systems_with_http_info

```ruby
begin
  # Detect anti-bot and CAPTCHA systems
  data, status_code, headers = api_instance.web_detect_anti_bot_and_captcha_systems_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_detect_anti_bot_and_captcha_systems_with_http_info: #{e}"
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


## web_extract_structured_data

> Object web_extract_structured_data

Extract structured data

Extract structured data from a URL using CSS or XPath selectors. (Phase 6)

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

api_instance = ScrapeBadger::WebApi.new

begin
  # Extract structured data
  result = api_instance.web_extract_structured_data
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_extract_structured_data: #{e}"
end
```

#### Using the web_extract_structured_data_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> web_extract_structured_data_with_http_info

```ruby
begin
  # Extract structured data
  data, status_code, headers = api_instance.web_extract_structured_data_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_extract_structured_data_with_http_info: #{e}"
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


## web_get_batch_job_status

> Object web_get_batch_job_status(job_id)

Get batch job status

Get the status of a batch scraping job. (Phase 6)

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

api_instance = ScrapeBadger::WebApi.new
job_id = 'job_id_example' # String | 

begin
  # Get batch job status
  result = api_instance.web_get_batch_job_status(job_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_get_batch_job_status: #{e}"
end
```

#### Using the web_get_batch_job_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> web_get_batch_job_status_with_http_info(job_id)

```ruby
begin
  # Get batch job status
  data, status_code, headers = api_instance.web_get_batch_job_status_with_http_info(job_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_get_batch_job_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **job_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## web_poll_an_auto_unblock_discovery_job

> Object web_poll_an_auto_unblock_discovery_job(job_id)

Poll an auto-unblock discovery job

Return the status + progress narration for an auto-unblock job.  Polled by the playground loader. ``job_id`` is an unguessable UUID handed out in the ``202 unblocking`` envelope and acts as a capability token, so any authenticated caller holding it can read the job (this is what lets several users share one discovery run's loader).

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

api_instance = ScrapeBadger::WebApi.new
job_id = 'job_id_example' # String | 

begin
  # Poll an auto-unblock discovery job
  result = api_instance.web_poll_an_auto_unblock_discovery_job(job_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_poll_an_auto_unblock_discovery_job: #{e}"
end
```

#### Using the web_poll_an_auto_unblock_discovery_job_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> web_poll_an_auto_unblock_discovery_job_with_http_info(job_id)

```ruby
begin
  # Poll an auto-unblock discovery job
  data, status_code, headers = api_instance.web_poll_an_auto_unblock_discovery_job_with_http_info(job_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_poll_an_auto_unblock_discovery_job_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **job_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## web_scrape_a_url

> Object web_scrape_a_url

Scrape a URL

Scrape a URL and return its content.  The Generic Web Scraping API is fully user-driven: callers pick their own request parameters (engine, proxy tier, country, JS rendering, …). A blocked target surfaces the raw 422 ``blocking_page_detected`` so the caller can tune parameters themselves — we do NOT auto-trigger host discovery. Curated per-origin overrides (which the dedicated scraper APIs depend on) still apply.

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

api_instance = ScrapeBadger::WebApi.new

begin
  # Scrape a URL
  result = api_instance.web_scrape_a_url
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_scrape_a_url: #{e}"
end
```

#### Using the web_scrape_a_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> web_scrape_a_url_with_http_info

```ruby
begin
  # Scrape a URL
  data, status_code, headers = api_instance.web_scrape_a_url_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_scrape_a_url_with_http_info: #{e}"
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


## web_submit_batch_scraping_job

> Object web_submit_batch_scraping_job

Submit batch scraping job

Submit a batch of URLs for scraping. (Phase 6)

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

api_instance = ScrapeBadger::WebApi.new

begin
  # Submit batch scraping job
  result = api_instance.web_submit_batch_scraping_job
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_submit_batch_scraping_job: #{e}"
end
```

#### Using the web_submit_batch_scraping_job_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> web_submit_batch_scraping_job_with_http_info

```ruby
begin
  # Submit batch scraping job
  data, status_code, headers = api_instance.web_submit_batch_scraping_job_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_submit_batch_scraping_job_with_http_info: #{e}"
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


## web_take_a_screenshot

> Object web_take_a_screenshot

Take a screenshot

Take a screenshot of a URL. (Phase 2 — patchright engine)

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

api_instance = ScrapeBadger::WebApi.new

begin
  # Take a screenshot
  result = api_instance.web_take_a_screenshot
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_take_a_screenshot: #{e}"
end
```

#### Using the web_take_a_screenshot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> web_take_a_screenshot_with_http_info

```ruby
begin
  # Take a screenshot
  data, status_code, headers = api_instance.web_take_a_screenshot_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_take_a_screenshot_with_http_info: #{e}"
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


## web_web_scraper_health_check

> Object web_web_scraper_health_check

Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes ``/health`` at the root (no ``/api/v1`` prefix, unlike the other scraper services).  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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

api_instance = ScrapeBadger::WebApi.new

begin
  # Web scraper health check
  result = api_instance.web_web_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_web_scraper_health_check: #{e}"
end
```

#### Using the web_web_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> web_web_scraper_health_check_with_http_info

```ruby
begin
  # Web scraper health check
  data, status_code, headers = api_instance.web_web_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_web_scraper_health_check_with_http_info: #{e}"
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


## web_web_scraper_health_check_head

> Object web_web_scraper_health_check_head

Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes ``/health`` at the root (no ``/api/v1`` prefix, unlike the other scraper services).  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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

api_instance = ScrapeBadger::WebApi.new

begin
  # Web scraper health check
  result = api_instance.web_web_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_web_scraper_health_check_head: #{e}"
end
```

#### Using the web_web_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> web_web_scraper_health_check_head_with_http_info

```ruby
begin
  # Web scraper health check
  data, status_code, headers = api_instance.web_web_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling WebApi->web_web_scraper_health_check_head_with_http_info: #{e}"
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

