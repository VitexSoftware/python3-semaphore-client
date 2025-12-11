# InfoType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**version** | **str** |  | [optional] 
**ansible** | **str** |  | [optional] 
**web_host** | **str** |  | [optional] 
**use_remote_runner** | **bool** |  | [optional] 
**auth_methods** | **object** |  | [optional] 
**git_client** | **str** |  | [optional] 
**schedule_timezone** | **str** |  | [optional] 
**premium_features** | **object** |  | [optional] 

## Example

```python
from semaphore_client.models.info_type import InfoType

# TODO update the JSON string below
json = "{}"
# create an instance of InfoType from a JSON string
info_type_instance = InfoType.from_json(json)
# print the JSON string representation of the object
print(InfoType.to_json())

# convert the object into a dict
info_type_dict = info_type_instance.to_dict()
# create an instance of InfoType from a dict
info_type_from_dict = InfoType.from_dict(info_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


