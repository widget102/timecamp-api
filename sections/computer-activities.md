Computer activities and time
======

GET /activity
----------

Get all computer time entries for specific user and day.

GET parameters:
* date: ex: 2014-03-07
* (optional) user_id: ex: 640

Example:
`https://www.timecamp.com/third_party/api/activity/format/json/api_token/a36cabi96bba83f826/date/2014-03-07/user_id/640`

```json
[
  {
    "user_id":"640",
    "application_id":"6319",
    "end_time":"2014-03-07 07:08:17",
    "time_span":8,
    "window_title_id":"1",
    "end_date":"2014-03-07",
    "task_id":"0"
  }
]
```

GET /application
----------

Get applications.

GET parameters:
* application_ids: ex: 6319,2132 (application ids separated by commas)

Example:
`https://www.timecamp.com/third_party/api/application/format/json/api_token/a36cabi96bba83f826/application_ids/6319`

```json
{
  "6319":
    {
      "application_id":"6319",
      "app_name":"Internet",
      "aditional_info":"google.com",
      "full_name":null,
      "category_id":"6"
    }
}
```

GET /window_title
----------

Get window titles.

GET parameters:
* window_title_ids: ex: 1,2 (application ids separated by commas)

Example:
`https://www.timecamp.com/third_party/api/window_title/format/json/api_token/a36cabi96bba83f826/window_title_ids/1,2`

```json
{
  "1234":
    {
      "window_title_id":"1234",
      "window_title":"MS Word - Document 1"
    },
  "3423":
    {
      "window_title_id":"3423",
      "window_title":"Yahoo"
    }
}
```
