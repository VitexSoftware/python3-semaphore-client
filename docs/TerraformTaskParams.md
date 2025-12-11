# TerraformTaskParams


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan** | **bool** |  | [optional] 
**destroy** | **bool** |  | [optional] 
**auto_approve** | **bool** |  | [optional] 
**upgrade** | **bool** |  | [optional] 

## Example

```python
from semaphore_client.models.terraform_task_params import TerraformTaskParams

# TODO update the JSON string below
json = "{}"
# create an instance of TerraformTaskParams from a JSON string
terraform_task_params_instance = TerraformTaskParams.from_json(json)
# print the JSON string representation of the object
print(TerraformTaskParams.to_json())

# convert the object into a dict
terraform_task_params_dict = terraform_task_params_instance.to_dict()
# create an instance of TerraformTaskParams from a dict
terraform_task_params_from_dict = TerraformTaskParams.from_dict(terraform_task_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


