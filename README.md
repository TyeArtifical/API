# Tye AI API
Recently, we have released an API for Tye. Heres how you can use it.

> [!WARNING]
> This API is experimental

## Generating a key
To generate a key, click [here](http://141.147.118.157:5678/webhook/4143f74e-3d1c-498e-be5f-a91d3a7a0a29).

Here’s a cleaner, more user-friendly version of your API usage section with clearer placeholders, better formatting, and cross-platform curl examples:

---

## Using the API

You can send a request to the webhook using a `POST` call with JSON data.

### Example (Windows CMD)

```bash
curl -X POST "http://141.147.118.157:5678/webhook/f9b818be-f507-436d-9af8-8ebd8270d049" ^
  -H "Content-Type: application/json" ^
  -d "{\"prompt\":\"hello\",\"sessionid\":\"0000000\",\"token\":\"XXXXX\"}"
```

### Example (Linux / macOS / Git Bash)

```bash
curl -X POST "http://141.147.118.157:5678/webhook/f9b818be-f507-436d-9af8-8ebd8270d049" \
  -H "Content-Type: application/json" \
  -d '{"prompt":"hello","sessionid":"0000000","token":"XXXXX"}'
```

---

## Parameters

* **prompt**: The message you want the AI to respond to.
* **sessionid**: A unique identifier for the user/session.
  👉 This is important for memory/context tracking. Use a consistent ID per user.
  UPDATE: This sessionid is now the API token so that API tokens can be revoked if it breaks the rules of Tye.
* **token**: Your API authentication token.

---

> [!NOTE]
> Always **replace `sessionid` with a unique value per user** (e.g., user ID, UUID, or database key). Aswell, keep `sessionid` consistent across requests for proper conversation memory. Never expose your real `token` publicly. Ensure JSON formatting is valid (especially when switching between Windows and Unix shells).

## Credits
Powered by [Stuf_y](https://github.com/StuffzEZ)'s API.
