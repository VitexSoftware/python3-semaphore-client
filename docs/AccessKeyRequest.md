# AccessKeyRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**project_id** | **int** |  | [optional] 
**override_secret** | **bool** |  | [optional] 
**login_password** | [**AccessKeyRequestLoginPassword**](AccessKeyRequestLoginPassword.md) |  | [optional] 
**ssh** | [**AccessKeyRequestSsh**](AccessKeyRequestSsh.md) |  | [optional] 

## Example

```python
from semaphore_client.models.access_key_request import AccessKeyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AccessKeyRequest from a JSON string
access_key_request_instance = AccessKeyRequest.from_json(json)
# print the JSON string representation of the object
print(AccessKeyRequest.to_json())

# convert the object into a dict
access_key_request_dict = access_key_request_instance.to_dict()
# create an instance of AccessKeyRequest from a dict
access_key_request_from_dict = AccessKeyRequest.from_dict(access_key_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


