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

GET /timer_running
----------

Get currently running timers.

Example:
`https://www.timecamp.com/third_party/api/timer_running/format/json/api_token/a36cabi96bba83f826`

```json
[
  {
    "timer_id":"31171",
    "user_id":"34365",
    "task_id":"1394831",
    "started_at":"2014-03-19 16:33:07",
    "name":"Development"
  }
]
```

GET /entries_changes
----------

Get manual changes in time entries made by users. This is only available only when it is enabled in Account Settings.

GET parameters:
* from - date range of the time entries returned like 2014-03-19
* to - date range of the time entries returned like 2014-03-19
* task_ids (optional) - tasks ids separated by commas, you can leave it empty, so it will get all tasks
* user_ids (optional) - user ids separated by commas, you can leave it empty, so it willl get all users

Example:
`https://www.timecamp.com/third_party/api/entries_changes/api_token/a36ca9cba8202/from/2014-03-19/to/2014-03-19/format/json`

```json
[
  {
    "entry_id":"353664",
    "old_time_span":"3960",
    "new_time_span":"3600",
    "edited":"2014-03-19 15:47:08",
    "user_id":"640",
    "description":"",
    "task_id":"1385384",
    "date":"2014-03-19",
    "start_time":"08:30:13",
    "end_time":"09:30:13",
    "locked":"0",
    "billable":1,
    "invoiceId":"0"
  }
]
```

