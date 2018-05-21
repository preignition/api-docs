---
description: Description of survey data API
---

# survey

{% api-method method="get" host="https://preignition.org/api" path="/v1/data/:programID/survey/:resourceID" %}
{% api-method-summary %}
Get Survey Data
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get survey data.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="resourceID" type="string" required=false %}
The ID of the resource \(survey\)
{% endapi-method-parameter %}

{% api-method-parameter name="programID" type="string" required=true %}
ID of the program
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
A valid token to identify the user initiating the request
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



