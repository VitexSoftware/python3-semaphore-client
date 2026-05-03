# semaphore_client.IntegrationApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**project_project_id_integrations_aliases_alias_id_delete**](IntegrationApi.md#project_project_id_integrations_aliases_alias_id_delete) | **DELETE** /project/{project_id}/integrations/aliases/{alias_id} | Remove integration alias
[**project_project_id_integrations_aliases_get**](IntegrationApi.md#project_project_id_integrations_aliases_get) | **GET** /project/{project_id}/integrations/aliases | Get all integration aliases for the project
[**project_project_id_integrations_aliases_post**](IntegrationApi.md#project_project_id_integrations_aliases_post) | **POST** /project/{project_id}/integrations/aliases | Create a new integration alias for the project
[**project_project_id_integrations_get**](IntegrationApi.md#project_project_id_integrations_get) | **GET** /project/{project_id}/integrations | get all integrations
[**project_project_id_integrations_integration_id_aliases_alias_id_delete**](IntegrationApi.md#project_project_id_integrations_integration_id_aliases_alias_id_delete) | **DELETE** /project/{project_id}/integrations/{integration_id}/aliases/{alias_id} | Remove integration alias
[**project_project_id_integrations_integration_id_aliases_get**](IntegrationApi.md#project_project_id_integrations_integration_id_aliases_get) | **GET** /project/{project_id}/integrations/{integration_id}/aliases | Get all aliases for an integration
[**project_project_id_integrations_integration_id_aliases_post**](IntegrationApi.md#project_project_id_integrations_integration_id_aliases_post) | **POST** /project/{project_id}/integrations/{integration_id}/aliases | Create a new alias for an integration
[**project_project_id_integrations_integration_id_delete**](IntegrationApi.md#project_project_id_integrations_integration_id_delete) | **DELETE** /project/{project_id}/integrations/{integration_id} | Remove integration
[**project_project_id_integrations_integration_id_get**](IntegrationApi.md#project_project_id_integrations_integration_id_get) | **GET** /project/{project_id}/integrations/{integration_id} | Get Integration
[**project_project_id_integrations_integration_id_matchers_get**](IntegrationApi.md#project_project_id_integrations_integration_id_matchers_get) | **GET** /project/{project_id}/integrations/{integration_id}/matchers | Get Integration Matcher linked to integration extractor
[**project_project_id_integrations_integration_id_matchers_matcher_id_delete**](IntegrationApi.md#project_project_id_integrations_integration_id_matchers_matcher_id_delete) | **DELETE** /project/{project_id}/integrations/{integration_id}/matchers/{matcher_id} | Removes integration matcher
[**project_project_id_integrations_integration_id_matchers_matcher_id_put**](IntegrationApi.md#project_project_id_integrations_integration_id_matchers_matcher_id_put) | **PUT** /project/{project_id}/integrations/{integration_id}/matchers/{matcher_id} | Updates Integration Matcher
[**project_project_id_integrations_integration_id_matchers_post**](IntegrationApi.md#project_project_id_integrations_integration_id_matchers_post) | **POST** /project/{project_id}/integrations/{integration_id}/matchers | Add Integration Matcher
[**project_project_id_integrations_integration_id_put**](IntegrationApi.md#project_project_id_integrations_integration_id_put) | **PUT** /project/{project_id}/integrations/{integration_id} | Update Integration
[**project_project_id_integrations_integration_id_values_extractvalue_id_delete**](IntegrationApi.md#project_project_id_integrations_integration_id_values_extractvalue_id_delete) | **DELETE** /project/{project_id}/integrations/{integration_id}/values/{extractvalue_id} | Removes integration extract value
[**project_project_id_integrations_integration_id_values_extractvalue_id_put**](IntegrationApi.md#project_project_id_integrations_integration_id_values_extractvalue_id_put) | **PUT** /project/{project_id}/integrations/{integration_id}/values/{extractvalue_id} | Updates Integration ExtractValue
[**project_project_id_integrations_integration_id_values_get**](IntegrationApi.md#project_project_id_integrations_integration_id_values_get) | **GET** /project/{project_id}/integrations/{integration_id}/values | Get Integration Extracted Values linked to integration extractor
[**project_project_id_integrations_integration_id_values_post**](IntegrationApi.md#project_project_id_integrations_integration_id_values_post) | **POST** /project/{project_id}/integrations/{integration_id}/values | Add Integration Extracted Value
[**project_project_id_integrations_post**](IntegrationApi.md#project_project_id_integrations_post) | **POST** /project/{project_id}/integrations | create a new integration


# **project_project_id_integrations_aliases_alias_id_delete**
> project_project_id_integrations_aliases_alias_id_delete(project_id, alias_id)

Remove integration alias

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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    alias_id = 15 # int | Integration Alias ID

    try:
        # Remove integration alias
        api_instance.project_project_id_integrations_aliases_alias_id_delete(project_id, alias_id)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_aliases_alias_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **alias_id** | **int**| Integration Alias ID | 

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
**204** | integration alias removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_aliases_get**
> List[IntegrationAlias] project_project_id_integrations_aliases_get(project_id)

Get all integration aliases for the project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_alias import IntegrationAlias
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # Get all integration aliases for the project
        api_response = api_instance.project_project_id_integrations_aliases_get(project_id)
        print("The response of IntegrationApi->project_project_id_integrations_aliases_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_aliases_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

### Return type

[**List[IntegrationAlias]**](IntegrationAlias.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Integration Aliases |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_aliases_post**
> IntegrationAlias project_project_id_integrations_aliases_post(project_id)

Create a new integration alias for the project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_alias import IntegrationAlias
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # Create a new integration alias for the project
        api_response = api_instance.project_project_id_integrations_aliases_post(project_id)
        print("The response of IntegrationApi->project_project_id_integrations_aliases_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_aliases_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

### Return type

[**IntegrationAlias**](IntegrationAlias.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Integration Alias Created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_get**
> List[Integration] project_project_id_integrations_get(project_id)

get all integrations

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration import Integration
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # get all integrations
        api_response = api_instance.project_project_id_integrations_get(project_id)
        print("The response of IntegrationApi->project_project_id_integrations_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

### Return type

[**List[Integration]**](Integration.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | integration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_aliases_alias_id_delete**
> project_project_id_integrations_integration_id_aliases_alias_id_delete(project_id, integration_id, alias_id)

Remove integration alias

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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID
    alias_id = 15 # int | Integration Alias ID

    try:
        # Remove integration alias
        api_instance.project_project_id_integrations_integration_id_aliases_alias_id_delete(project_id, integration_id, alias_id)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_aliases_alias_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 
 **alias_id** | **int**| Integration Alias ID | 

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
**204** | integration alias removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_aliases_get**
> List[IntegrationAlias] project_project_id_integrations_integration_id_aliases_get(project_id, integration_id)

Get all aliases for an integration

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_alias import IntegrationAlias
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID

    try:
        # Get all aliases for an integration
        api_response = api_instance.project_project_id_integrations_integration_id_aliases_get(project_id, integration_id)
        print("The response of IntegrationApi->project_project_id_integrations_integration_id_aliases_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_aliases_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 

### Return type

[**List[IntegrationAlias]**](IntegrationAlias.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Integration Aliases |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_aliases_post**
> IntegrationAlias project_project_id_integrations_integration_id_aliases_post(project_id, integration_id)

Create a new alias for an integration

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_alias import IntegrationAlias
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID

    try:
        # Create a new alias for an integration
        api_response = api_instance.project_project_id_integrations_integration_id_aliases_post(project_id, integration_id)
        print("The response of IntegrationApi->project_project_id_integrations_integration_id_aliases_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_aliases_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 

### Return type

[**IntegrationAlias**](IntegrationAlias.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Integration Alias Created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_delete**
> project_project_id_integrations_integration_id_delete(project_id, integration_id)

Remove integration

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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID

    try:
        # Remove integration
        api_instance.project_project_id_integrations_integration_id_delete(project_id, integration_id)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 

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
**204** | integration removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_get**
> Integration project_project_id_integrations_integration_id_get(project_id, integration_id)

Get Integration

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration import Integration
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID

    try:
        # Get Integration
        api_response = api_instance.project_project_id_integrations_integration_id_get(project_id, integration_id)
        print("The response of IntegrationApi->project_project_id_integrations_integration_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 

### Return type

[**Integration**](Integration.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Integration Value |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_matchers_get**
> List[IntegrationMatcher] project_project_id_integrations_integration_id_matchers_get(project_id, integration_id)

Get Integration Matcher linked to integration extractor

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_matcher import IntegrationMatcher
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID

    try:
        # Get Integration Matcher linked to integration extractor
        api_response = api_instance.project_project_id_integrations_integration_id_matchers_get(project_id, integration_id)
        print("The response of IntegrationApi->project_project_id_integrations_integration_id_matchers_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_matchers_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 

### Return type

[**List[IntegrationMatcher]**](IntegrationMatcher.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Integration Matcher |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_matchers_matcher_id_delete**
> project_project_id_integrations_integration_id_matchers_matcher_id_delete(project_id, integration_id, matcher_id)

Removes integration matcher

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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID
    matcher_id = 13 # int | matcher ID

    try:
        # Removes integration matcher
        api_instance.project_project_id_integrations_integration_id_matchers_matcher_id_delete(project_id, integration_id, matcher_id)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_matchers_matcher_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 
 **matcher_id** | **int**| matcher ID | 

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
**204** | integration matcher removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_matchers_matcher_id_put**
> project_project_id_integrations_integration_id_matchers_matcher_id_put(project_id, integration_id, matcher_id, integration_matcher_request)

Updates Integration Matcher

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_matcher_request import IntegrationMatcherRequest
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID
    matcher_id = 13 # int | matcher ID
    integration_matcher_request = semaphore_client.IntegrationMatcherRequest() # IntegrationMatcherRequest | 

    try:
        # Updates Integration Matcher
        api_instance.project_project_id_integrations_integration_id_matchers_matcher_id_put(project_id, integration_id, matcher_id, integration_matcher_request)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_matchers_matcher_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 
 **matcher_id** | **int**| matcher ID | 
 **integration_matcher_request** | [**IntegrationMatcherRequest**](IntegrationMatcherRequest.md)|  | 

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
**204** | Integration Matcher updated |  -  |
**400** | Bad integration matcher parameter |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_matchers_post**
> project_project_id_integrations_integration_id_matchers_post(project_id, integration_id, integration_matcher)

Add Integration Matcher

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_matcher import IntegrationMatcher
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID
    integration_matcher = semaphore_client.IntegrationMatcher() # IntegrationMatcher | 

    try:
        # Add Integration Matcher
        api_instance.project_project_id_integrations_integration_id_matchers_post(project_id, integration_id, integration_matcher)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_matchers_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 
 **integration_matcher** | [**IntegrationMatcher**](IntegrationMatcher.md)|  | 

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
**200** | Integration Matcher Created |  -  |
**400** | Bad Integration Matcher params |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_put**
> project_project_id_integrations_integration_id_put(project_id, integration_id, integration_request)

Update Integration

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_request import IntegrationRequest
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID
    integration_request = semaphore_client.IntegrationRequest() # IntegrationRequest | 

    try:
        # Update Integration
        api_instance.project_project_id_integrations_integration_id_put(project_id, integration_id, integration_request)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 
 **integration_request** | [**IntegrationRequest**](IntegrationRequest.md)|  | 

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
**204** | Integration updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_values_extractvalue_id_delete**
> project_project_id_integrations_integration_id_values_extractvalue_id_delete(project_id, integration_id, extractvalue_id)

Removes integration extract value

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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID
    extractvalue_id = 12 # int | extractValue ID

    try:
        # Removes integration extract value
        api_instance.project_project_id_integrations_integration_id_values_extractvalue_id_delete(project_id, integration_id, extractvalue_id)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_values_extractvalue_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 
 **extractvalue_id** | **int**| extractValue ID | 

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
**204** | integration extract value removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_values_extractvalue_id_put**
> project_project_id_integrations_integration_id_values_extractvalue_id_put(project_id, integration_id, extractvalue_id, integration_extract_value_request)

Updates Integration ExtractValue

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_extract_value_request import IntegrationExtractValueRequest
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID
    extractvalue_id = 12 # int | extractValue ID
    integration_extract_value_request = semaphore_client.IntegrationExtractValueRequest() # IntegrationExtractValueRequest | 

    try:
        # Updates Integration ExtractValue
        api_instance.project_project_id_integrations_integration_id_values_extractvalue_id_put(project_id, integration_id, extractvalue_id, integration_extract_value_request)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_values_extractvalue_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 
 **extractvalue_id** | **int**| extractValue ID | 
 **integration_extract_value_request** | [**IntegrationExtractValueRequest**](IntegrationExtractValueRequest.md)|  | 

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
**204** | Integration Extract Value updated |  -  |
**400** | Bad integration extract value parameter |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_values_get**
> List[IntegrationExtractValue] project_project_id_integrations_integration_id_values_get(project_id, integration_id)

Get Integration Extracted Values linked to integration extractor

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_extract_value import IntegrationExtractValue
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID

    try:
        # Get Integration Extracted Values linked to integration extractor
        api_response = api_instance.project_project_id_integrations_integration_id_values_get(project_id, integration_id)
        print("The response of IntegrationApi->project_project_id_integrations_integration_id_values_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_values_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 

### Return type

[**List[IntegrationExtractValue]**](IntegrationExtractValue.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Integration Extracted Value |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_integration_id_values_post**
> project_project_id_integrations_integration_id_values_post(project_id, integration_id, integration_extract_value)

Add Integration Extracted Value

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration_extract_value import IntegrationExtractValue
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_id = 11 # int | integration ID
    integration_extract_value = semaphore_client.IntegrationExtractValue() # IntegrationExtractValue | 

    try:
        # Add Integration Extracted Value
        api_instance.project_project_id_integrations_integration_id_values_post(project_id, integration_id, integration_extract_value)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_integration_id_values_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_id** | **int**| integration ID | 
 **integration_extract_value** | [**IntegrationExtractValue**](IntegrationExtractValue.md)|  | 

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
**201** | Integration Extract Value Created |  -  |
**400** | Bad Integration Extract Value params |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_integrations_post**
> Integration project_project_id_integrations_post(project_id, integration_request)

create a new integration

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.integration import Integration
from semaphore_client.models.integration_request import IntegrationRequest
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
    api_instance = semaphore_client.IntegrationApi(api_client)
    project_id = 1 # int | Project ID
    integration_request = semaphore_client.IntegrationRequest() # IntegrationRequest | 

    try:
        # create a new integration
        api_response = api_instance.project_project_id_integrations_post(project_id, integration_request)
        print("The response of IntegrationApi->project_project_id_integrations_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IntegrationApi->project_project_id_integrations_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **integration_request** | [**IntegrationRequest**](IntegrationRequest.md)|  | 

### Return type

[**Integration**](Integration.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Integration Created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

