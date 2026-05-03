# IntegrationAlias


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**url** | **str** |  | [optional] 

## Example

```python
from semaphore_client.models.integration_alias import IntegrationAlias

# TODO update the JSON string below
json = "{}"
# create an instance of IntegrationAlias from a JSON string
integration_alias_instance = IntegrationAlias.from_json(json)
# print the JSON string representation of the object
print(IntegrationAlias.to_json())

# convert the object into a dict
integration_alias_dict = integration_alias_instance.to_dict()
# create an instance of IntegrationAlias from a dict
integration_alias_from_dict = IntegrationAlias.from_dict(integration_alias_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


