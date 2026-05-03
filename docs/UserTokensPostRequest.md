# UserTokensPostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 

## Example

```python
from semaphore_client.models.user_tokens_post_request import UserTokensPostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UserTokensPostRequest from a JSON string
user_tokens_post_request_instance = UserTokensPostRequest.from_json(json)
# print the JSON string representation of the object
print(UserTokensPostRequest.to_json())

# convert the object into a dict
user_tokens_post_request_dict = user_tokens_post_request_instance.to_dict()
# create an instance of UserTokensPostRequest from a dict
user_tokens_post_request_from_dict = UserTokensPostRequest.from_dict(user_tokens_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


