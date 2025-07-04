# A.X 4.0 API documents

This API documents describes the RESTful APIs that you can interact with **A.X 4.0** 

## Authentication

**A.X 4.0 APIs are FREE now!** We provide public key for anonymous users.
```bash
ADOTX_API_KEY="sktax-XyeKFrq67ZjS4EpsDlrHHXV8it"
```

## Create a A.X 4.0 model response

`POST https://guest-api.sktax.chat/v1`

### CURL

```bash
# Request
ADOTX_API_KEY="sktax-XyeKFrq67ZjS4EpsDlrHHXV8it"
curl https://guest-api.sktax.chat/v1/chat/completions \
    -H "Content-Type: application/json" \
    -H "Authorization: Bearer $ADOTX_API_KEY" \
    -d '{
        "model": "ax4",
        "messages": [
            {"role": "user", "content": "여름철 에어컨 적정 온도는? 한줄로 대답해."}
        ]
    }'
```

```bash
# Response
{
    "id": "chatcmpl-c8775b82979ad5aa77a3bb66a9d6b504",
    "object": "chat.completion",
    "created": 1751605552,
    "model": "ax4",
    "choices": [
        {
            "index": 0,
            "message": {
                "role": "assistant",
                "reasoning_content": null,
                "content": "여름철 에어컨 적정 온도는 24~26도입니다.",
                "tool_calls": []
            },
            "logprobs": null,
            "finish_reason": "stop",
            "stop_reason": null
        }
    ],
    "usage": {
        "prompt_tokens": 15,
        "total_tokens": 27,
        "completion_tokens": 12,
        "prompt_tokens_details": null
    },
    "prompt_logprobs": null
}
```

### PYTHON

```python
# Request
from openai import OpenAI

client = OpenAI(
    base_url="https://guest-api.sktax.chat/v1",
    api_key="sktax-XyeKFrq67ZjS4EpsDlrHHXV8it"
)

completion = client.chat.completions.create(
    model="ax4",
    messages=[
        {"role": "user", "content": "여름철 에어컨 적정 온도는? 한줄로 대답해."}
    ]
)

print(completion)
```

```python
# Response
ChatCompletion(
    id='chatcmpl-91de86607d222481e30fc057403c8da8', 
    choices=[
        Choice(
            finish_reason='stop', 
            index=0, 
            logprobs=None, 
            message=ChatCompletionMessage(
                content='여름철 에어컨 적정 온도는 26도 내외입니다.', 
                role='assistant', 
                function_call=None, 
                tool_calls=[], 
                reasoning_content=None
            ), 
            stop_reason=None
        )
    ], 
    created=1751605927, 
    model='ax4', 
    object='chat.completion', 
    system_fingerprint=None, 
    usage=CompletionUsage(
        completion_tokens=11, 
        prompt_tokens=15, 
        total_tokens=26, 
        prompt_tokens_details=None
    ), 
    prompt_logprobs=None
)
```
