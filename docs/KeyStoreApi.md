# semaphore_client.KeyStoreApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**project_project_id_keys_get**](KeyStoreApi.md#project_project_id_keys_get) | **GET** /project/{project_id}/keys | Get access keys linked to project
[**project_project_id_keys_key_id_delete**](KeyStoreApi.md#project_project_id_keys_key_id_delete) | **DELETE** /project/{project_id}/keys/{key_id} | Removes access key
[**project_project_id_keys_key_id_put**](KeyStoreApi.md#project_project_id_keys_key_id_put) | **PUT** /project/{project_id}/keys/{key_id} | Updates access key
[**project_project_id_keys_post**](KeyStoreApi.md#project_project_id_keys_post) | **POST** /project/{project_id}/keys | Add access key


# **project_project_id_keys_get**
> List[AccessKey] project_project_id_keys_get(project_id, sort, order, key_type=key_type)

Get access keys linked to project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.access_key import AccessKey
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
    api_instance = semaphore_client.KeyStoreApi(api_client)
    project_id = 1 # int | Project ID
    sort = 'type' # str | sorting name
    order = 'asc' # str | ordering manner
    key_type = 'none' # str | Filter by key type (optional)

    try:
        # Get access keys linked to project
        api_response = api_instance.project_project_id_keys_get(project_id, sort, order, key_type=key_type)
        print("The response of KeyStoreApi->project_project_id_keys_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KeyStoreApi->project_project_id_keys_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **sort** | **str**| sorting name | 
 **order** | **str**| ordering manner | 
 **key_type** | **str**| Filter by key type | [optional] 

### Return type

[**List[AccessKey]**](AccessKey.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Access Keys |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_keys_key_id_delete**
> project_project_id_keys_key_id_delete(project_id, key_id)

Removes access key

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
    api_instance = semaphore_client.KeyStoreApi(api_client)
    project_id = 1 # int | Project ID
    key_id = 3 # int | key ID

    try:
        # Removes access key
        api_instance.project_project_id_keys_key_id_delete(project_id, key_id)
    except Exception as e:
        print("Exception when calling KeyStoreApi->project_project_id_keys_key_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **key_id** | **int**| key ID | 

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
**204** | access key removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_keys_key_id_put**
> project_project_id_keys_key_id_put(project_id, key_id, access_key_request)

Updates access key

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.access_key_request import AccessKeyRequest
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
    api_instance = semaphore_client.KeyStoreApi(api_client)
    project_id = 1 # int | Project ID
    key_id = 3 # int | key ID
    access_key_request = semaphore_client.AccessKeyRequest() # AccessKeyRequest | 

    try:
        # Updates access key
        api_instance.project_project_id_keys_key_id_put(project_id, key_id, access_key_request)
    except Exception as e:
        print("Exception when calling KeyStoreApi->project_project_id_keys_key_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **key_id** | **int**| key ID | 
 **access_key_request** | [**AccessKeyRequest**](AccessKeyRequest.md)|  | 

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
**204** | Key updated |  -  |
**400** | Bad type |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_keys_post**
> AccessKey project_project_id_keys_post(project_id, access_key_request)

Add access key

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.access_key import AccessKey
from semaphore_client.models.access_key_request import AccessKeyRequest
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
    api_instance = semaphore_client.KeyStoreApi(api_client)
    project_id = 1 # int | Project ID
    access_key_request = semaphore_client.AccessKeyRequest() # AccessKeyRequest | 

    try:
        # Add access key
        api_response = api_instance.project_project_id_keys_post(project_id, access_key_request)
        print("The response of KeyStoreApi->project_project_id_keys_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KeyStoreApi->project_project_id_keys_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **access_key_request** | [**AccessKeyRequest**](AccessKeyRequest.md)|  | 

### Return type

[**AccessKey**](AccessKey.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Access Key created |  -  |
**400** | Bad type |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

