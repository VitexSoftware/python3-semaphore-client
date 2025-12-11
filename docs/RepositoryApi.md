# semaphore_client.RepositoryApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**project_project_id_repositories_get**](RepositoryApi.md#project_project_id_repositories_get) | **GET** /project/{project_id}/repositories | Get repositories
[**project_project_id_repositories_post**](RepositoryApi.md#project_project_id_repositories_post) | **POST** /project/{project_id}/repositories | Add repository
[**project_project_id_repositories_repository_id_delete**](RepositoryApi.md#project_project_id_repositories_repository_id_delete) | **DELETE** /project/{project_id}/repositories/{repository_id} | Removes repository
[**project_project_id_repositories_repository_id_get**](RepositoryApi.md#project_project_id_repositories_repository_id_get) | **GET** /project/{project_id}/repositories/{repository_id} | Get repository
[**project_project_id_repositories_repository_id_put**](RepositoryApi.md#project_project_id_repositories_repository_id_put) | **PUT** /project/{project_id}/repositories/{repository_id} | Updates repository


# **project_project_id_repositories_get**
> List[Repository] project_project_id_repositories_get(project_id, sort, order)

Get repositories

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.repository import Repository
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.RepositoryApi(api_client)
    project_id = 1 # int | Project ID
    sort = 'sort_example' # str | sorting name
    order = 'order_example' # str | ordering manner

    try:
        # Get repositories
        api_response = api_instance.project_project_id_repositories_get(project_id, sort, order)
        print("The response of RepositoryApi->project_project_id_repositories_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RepositoryApi->project_project_id_repositories_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **sort** | **str**| sorting name | 
 **order** | **str**| ordering manner | 

### Return type

[**List[Repository]**](Repository.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | repositories |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_repositories_post**
> Repository project_project_id_repositories_post(project_id, repository_request)

Add repository

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.repository import Repository
from semaphore_client.models.repository_request import RepositoryRequest
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.RepositoryApi(api_client)
    project_id = 1 # int | Project ID
    repository_request = semaphore_client.RepositoryRequest() # RepositoryRequest | 

    try:
        # Add repository
        api_response = api_instance.project_project_id_repositories_post(project_id, repository_request)
        print("The response of RepositoryApi->project_project_id_repositories_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RepositoryApi->project_project_id_repositories_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **repository_request** | [**RepositoryRequest**](RepositoryRequest.md)|  | 

### Return type

[**Repository**](Repository.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Repository created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_repositories_repository_id_delete**
> project_project_id_repositories_repository_id_delete(project_id, repository_id)

Removes repository

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.RepositoryApi(api_client)
    project_id = 1 # int | Project ID
    repository_id = 4 # int | repository ID

    try:
        # Removes repository
        api_instance.project_project_id_repositories_repository_id_delete(project_id, repository_id)
    except Exception as e:
        print("Exception when calling RepositoryApi->project_project_id_repositories_repository_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **repository_id** | **int**| repository ID | 

### Return type

void (empty response body)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | repository removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_repositories_repository_id_get**
> Repository project_project_id_repositories_repository_id_get(project_id, repository_id)

Get repository

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.repository import Repository
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.RepositoryApi(api_client)
    project_id = 1 # int | Project ID
    repository_id = 4 # int | repository ID

    try:
        # Get repository
        api_response = api_instance.project_project_id_repositories_repository_id_get(project_id, repository_id)
        print("The response of RepositoryApi->project_project_id_repositories_repository_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RepositoryApi->project_project_id_repositories_repository_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **repository_id** | **int**| repository ID | 

### Return type

[**Repository**](Repository.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | repository object |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_repositories_repository_id_put**
> project_project_id_repositories_repository_id_put(project_id, repository_id, repository_request)

Updates repository

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.repository_request import RepositoryRequest
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.RepositoryApi(api_client)
    project_id = 1 # int | Project ID
    repository_id = 4 # int | repository ID
    repository_request = semaphore_client.RepositoryRequest() # RepositoryRequest | 

    try:
        # Updates repository
        api_instance.project_project_id_repositories_repository_id_put(project_id, repository_id, repository_request)
    except Exception as e:
        print("Exception when calling RepositoryApi->project_project_id_repositories_repository_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **repository_id** | **int**| repository ID | 
 **repository_request** | [**RepositoryRequest**](RepositoryRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Repository updated |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

