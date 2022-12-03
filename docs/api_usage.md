# API Usage

This is the API documentation for [XenoAI](https://xeno-ai.space)

- [Python](#python-example)
- [Nodejs](#nodejs-example)
- [cURL](#curl-example)

### Example Response

```json
{
    "version": "2.2.4", // The current version of the api
    "output": "https://api.xeno-ai.space/content/b33c89457945cac", // Combined
    "images": [
        "https://api.xeno-ai.space/content/bc087fbca2188", // Image 1
        "https://api.xeno-ai.space/content/0ed3badc727b0", // Image 2
        "https://api.xeno-ai.space/content/c6d3abd73ffda" // Image 3
    ]
}
```

Content-Type: application/json

!!! note "Important Information"

    Please replace the <PROMPT\> and <API_KEY\> with your own information.
    If you use the /demo/images enpoint instead you will get rate limited,
    check out [Rate Limits](/rate_limits) for more information.

## Python Example

```python
import requests
import json

url = "https://api.xeno-ai.space/images"

payload = json.dumps({
"prompt": "<PROMPT>"
})
headers = {
'Authorization': '<API_KEY>',
'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)
```

## Nodejs Example

```js
var axios = require('axios');
var data = JSON.stringify({
  "prompt": "<PROMPT>"
});

var config = {
  method: 'post',
  url: 'https://api.xeno-ai.space/images',
  headers: { 
    'Authorization': '<API_KEY>', 
    'Content-Type': 'application/json'
  },
  data : data
};

axios(config)
.then(function (response) {
  console.log(JSON.stringify(response.data));
})
.catch(function (error) {
  console.log(error);
});
```

## cURL Example

```bash
curl --location --request POST 'https://api.xeno-ai.space/images' \
--header 'Authorization: <API_KEY>' \
--header 'Content-Type: application/json' \
--data-raw '{"prompt": "<PROMPT>}'
```




