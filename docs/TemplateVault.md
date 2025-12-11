# TemplateVault


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**vault_key_id** | **int** |  | [optional] 
**script** | **str** |  | [optional] 

## Example

```python
from semaphore_client.models.template_vault import TemplateVault

# TODO update the JSON string below
json = "{}"
# create an instance of TemplateVault from a JSON string
template_vault_instance = TemplateVault.from_json(json)
# print the JSON string representation of the object
print(TemplateVault.to_json())

# convert the object into a dict
template_vault_dict = template_vault_instance.to_dict()
# create an instance of TemplateVault from a dict
template_vault_from_dict = TemplateVault.from_dict(template_vault_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


