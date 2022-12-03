# API Endpoints

This page contains all API endpoints <br />
API url [https://api.xeno-ai.space](https://api.xeno-ai.space)

- [Demo Endpoint](#demo-endpoint)
- [Images Endpoint](#images-endpoint)

## Demo Endpoint 

`POST` **/demo/images** 

This endpoint can be used to try out our API without an API key,
but is rate limited check [Rate Limits](/rate_limits) for more info.

### Example JSON Request

```json
{
    "prompt": "a cat floating in space, realistic 8k"
}
```

!!! note "Information"

    Generating an image should not take longer then 15 seconds, if so it means we have a high traffic at the moment.

### Example JSON Response

```json
{
    "version": "2.2.4",
    "images": [
        "https://api.xeno-ai.space/content/bc087fbca2188",
        "https://api.xeno-ai.space/content/0ed3badc727b0",
        "https://api.xeno-ai.space/content/c6d3abd73ffda"
    ]
}
```

## Images Endpoint 

`POST` **/images** 

This endpoint is used for production applications and requires an Authorization header with an API key.
We do not rate limit this endpoint normaly but we do when our servers are on heavy load.

### Example JSON Request

```yaml
Authorization: <YOUR_API_KEY>
```

```json
{
    "prompt": "a house on a mountain, realistic, dark background"
}
```

!!! note "Information"

    Generating an image should not take longer then 15 seconds, if so it means we have a high traffic at the moment.

### Example JSON Response

```json
{
    "version": "2.2.4",
    "output": "https://api.xeno-ai.space/content/b33c89457945cac",
    "images": [
        "https://api.xeno-ai.space/content/bc087fbca2188",
        "https://api.xeno-ai.space/content/0ed3badc727b0",
        "https://api.xeno-ai.space/content/c6d3abd73ffda"
    ]
}
```



