Time entries
======

GET /entries
----------

Get time entries started in a specific time range.

GET parameters:
* task_ids - tasks ids separated by commas, you can leave it empty, so it will get all tasks
* (optional) with_subtasks = 1, get entries for all subtasks for provided one specific task_ids, put in the url: with_subtasks/1
* user_ids - user ids separated by commas, you can leave it empty, so it willl get all users
* from - date range of the time entries returned
* to - date range of the time entries returned

Example:
`https://www.timecamp.com/third_party/api/entries/format/json/api_token/a36cabi96bba83f826/from/2013-02-01/to/2013-03-20/task_ids/3132,3241/user_ids/123`

```json
[
  {
    "id":"3621",
    "duration":"3600",
    "user_id":"123",
    "description":"",
    "task_id":"3132",
    "date":"2013-03-30",
    "start_time":"12:20:00", (this value may be null if user didn’t specify time frame)
    “name”:”Task name”,
    “addons_external_id”:123241 (for integrations with Trello, Pivotal Tracker, etc.)
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

