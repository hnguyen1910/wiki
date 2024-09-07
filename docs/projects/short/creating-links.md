---
description: This page shows you how to create a new shortened link.
---

# Creating Links

### Base URL:

```
https://r.tinvn.eu.org/api
```

### Endpoints:

<mark style="color:green;">`GET`</mark> `/new`

**Query Parameters**

| Name            | Type   | Description                    |
| --------------- | ------ | ------------------------------ |
| `url`(required) | string | URL that needs to be shortened |

#### Example Request

{% tabs %}
{% tab title="cURL (cmd)" %}
```
curl -X GET "https://r.tinvn.eu.org/api/new?url=<url>" 
```
{% endtab %}

{% tab title="requests (Python)" %}
<pre class="language-python"><code class="lang-python"><strong>import requests
</strong><strong>
</strong><strong>response = requests.get(
</strong>  url = "https://r.tinvn.eu.org/api/new",
  params = {
    "url" : &#x3C;url>
    }
  )
  
print(response.json())
</code></pre>
{% endtab %}
{% endtabs %}

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
  "id": 1, 
  "message": "OK", 
  "original_url": "https://example.com", 
  "short_id": "JxMaxj", 
  "short_url": "http://r.tinvn.eu.org/JxMaxj", 
  "status": 200
}
```
{% endtab %}
{% endtabs %}

#### Errors

<table><thead><tr><th width="120">Code</th><th>Description</th></tr></thead><tbody><tr><td>ER1</td><td>You didn't provide a url.</td></tr><tr><td>ER2</td><td>Invaild URL provided.</td></tr></tbody></table>
