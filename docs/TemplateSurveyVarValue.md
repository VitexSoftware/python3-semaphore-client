# TemplateSurveyVarValue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**value** | **str** |  | [optional] 

## Example

```python
from semaphore_client.models.template_survey_var_value import TemplateSurveyVarValue

# TODO update the JSON string below
json = "{}"
# create an instance of TemplateSurveyVarValue from a JSON string
template_survey_var_value_instance = TemplateSurveyVarValue.from_json(json)
# print the JSON string representation of the object
print(TemplateSurveyVarValue.to_json())

# convert the object into a dict
template_survey_var_value_dict = template_survey_var_value_instance.to_dict()
# create an instance of TemplateSurveyVarValue from a dict
template_survey_var_value_from_dict = TemplateSurveyVarValue.from_dict(template_survey_var_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


