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

POST /time_entry
----------

Add a new time entry.

Example:
`https://www.timecamp.com/third_party/api/time_entry/api_token/a36cabi96bba83f826`

Post Fields:
* task_id: 13 (from our API)
* duration: 3600 (in seconds)
* date: ‘2013-06-06’
* note: ‘custom note’ (optional)
* start: ‘13:30’ (optional)
* stop: ‘14:23’ (optional)

