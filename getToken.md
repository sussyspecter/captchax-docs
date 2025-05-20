---
markdown:
    toc:
        depth: 2
---
# getToken

Effortlessly integrate the **getToken** API to bypass any Captcha. This streamlined endpoint delivers the solution token in a single request, ensuring a reliable automation workflow.

```http {% title="HTTP Request" %}
POST https://api.captchax.ai/getToken HTTP/1.1
Host: api.captchax.ai
Content-Type: application/json
```

## Request Parameters

### Top-Level Parameters

| Parameter | Type   | Required | Description                             |
| :-------- | :----- | :------- | :-------------------------------------- |
| `info`    | Object | Yes      | Contains information about the request. |
| `params`  | Object | Yes      | Contains task-specific parameters.      |

### `info` Object Parameters

| Parameter     | Type   | Required | Description                                                       |
| :------------ | :----- | :------- | :---------------------------------------------------------------- |
| `api_service` | String | Yes      | The type of task to create. Refer to **Supported CAPTCHA Types**. |
| `api_token`   | String | Yes      | Your API key to authenticate the request.                         |

### `params` Object Parameters

These parameters depend on the task type. Refer to information in the task's documetation page.

## Example Request

```json
{
    "info": {
        "api_service": "ReCaptchaV2",
        "api_token": "YOUR_API_KEY"
    },
    "params": {
        "websiteURL": "https://www.google.com/recaptcha/api2/demo",
        "websiteKey": "6Le-wvkSAAAAAPBMRTvw0Q4Muexq9bi0DJwx_mJ-"
    }
}
```

## Example Response

```json {% title="Success Response" %}
{
    "data": {
        "token": "03AFcWeA7vQiFmaYZWoYWht...",
        "createTime": 1745415127693,
        "endTime": 1745415127693
    },
    "error": false,
    "message": "Success"
}
```

```json {% title="Error Response" %}
{
    "error": true,
    "message": "Customer not found with credit balance"
}
```
