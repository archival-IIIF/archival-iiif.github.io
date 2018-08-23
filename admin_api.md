# Admin API Documentation

All requests require an access token. Use the `access_token` parameter.

## Index API

````
POST: /admin/index_api
````

__Input body__

 * Manifest container json file 
 
 ```
 {
    "id": "My collection",
    "items": [
      {
        "id": "12345",
        "parent_id": null,
        "collection_id": "My collection",
        "type": "folder",
        "label": "My folder",
        "size": null,
        "created_at": null,
        "width": null,
        "height": null,
        "original": {
            "uri": null,
            "puid": null
        },
        "access": {
            "uri": null,
            "puid": null
        }
      },
      ...
    ]
 }
 ```
 
## Index 

````
POST: /admin/index
````

__Input parameters__

 * `path` The path to the collection to be indexed
 
 ## Register token 
 
 ````
 POST: /admin/register_token
 ````
 
 __Input parameters__
 
  * `token` The token to register
  * `collection` The collection to which this token provides access
  * `from` The date from which it is valid
  * `to` The date till which it is valid
 