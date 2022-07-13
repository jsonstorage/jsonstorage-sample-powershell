# jsonstorage-sample-powershell

## Create JSON:

```
$url = "https://api.jsonstorage.net/v1/json?apiKey=<your api key>"
$body = @{
    "siteUrl" ="https://example.com"
    "email" = "info@example.com"
}

Invoke-RestMethod -Method 'Post' -Uri $url -Body ($body|ConvertTo-Json) -ContentType "application/json"
````

## Update JSON:

```
$url = "https://api.jsonstorage.net/v1/json/<userId>/<itemId>?apiKey=<your api key>"
$body = @{
    "siteUrl" ="https://update-example.com"
    "email" = "info@update-example.com"
}

Invoke-RestMethod -Method 'Put' -Uri $url -Body ($body|ConvertTo-Json) -ContentType "application/json"
````

## Delete JSON:

```
$url = "https://api.jsonstorage.net/v1/json/<itemId>?apiKey=<your api key>"

Invoke-RestMethod -Method 'Delete' -Uri $url  -ContentType "application/json"
````
