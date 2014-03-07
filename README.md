TimeCamp API
====================

This is a REST-style API. TimeCamp API lets you do some basic things with tasks. You can contact us at [dev@timecamp.com](mailto:dev@timecamp.com). We are very open to new ideas and requests regarding API.


Making a request
----------------

All URLs start with `https://www.timecamp.com/third_party/api`. **SSL only**.
That's all!


Authentication
--------------

Authentication is very simple. You must put your API token in every API request. You can provide API token in POST or GET http method. The name for API token field is: api_token
Example:
`https://www.timecamp.com/third_party/api/tasks/format/json/api_token/a36cabi96bba83f826`

**To get your API token please go to your [Account Settings](https://www.timecamp.com/people/edit).**


Result data formats
---------------

* xml (default)
* json
* csv
* other: rawxml, jsonp, serialized, php, html 

Example:
`https://www.timecamp.com/third_party/api/tasks/format/json/api_token/a36cabi96bba83f826`


Handling errors
---------------

If a API request failed, an array of localized error messages and error code will be returned.
Response example:
```json
{
"message":"sample message",
"code":401
}
```

Rate limiting
-------------

For this moment there is no rate limits.


API ready for use
-----------------

* [Users](https://github.com/basecamp/bcx-api/blob/master/sections/projects.md)
* [Tasks](https://github.com/basecamp/bcx-api/blob/master/sections/people.md)
* [Time entries](https://github.com/basecamp/bcx-api/blob/master/sections/accesses.md)
* [Computer activities](https://github.com/basecamp/bcx-api/blob/master/sections/events.md)


Examples
-----------------

* [PHP Examples](https://github.com/timecamp2/timecamp-api/blob/master/sections/php-examples.md)
