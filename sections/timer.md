Timer
======

POST /timer
----------

Add a new time entry.

Example:
`https://www.timecamp.com/third_party/api/timer/api_token/a36cabi96bba83f826`

Post Variable Array Fields:
* action: "start" (__required__)
* task_id: 123 (optional)
* entry_id: "create" (optional)
* started_at: ‘2016-04-19 10:50:11’ (uses current time if omitted)

Response:
{
    "new_timer_id": 1420259,
    "entry_id": 8780527
}

----------

To get status of current timer:

Post Variable Array Fields:
* action: "status"

Response:
{
    "isTimerRunning": true,
    "elapsed": 319,
    "entry_id": "8780527",
    "timer_id": "1420259",
    "start_time": "2016-04-19 10:50:11",
    "task_id": "7536867",
    "name": "Brazil",
    "external_task_id": null
}

----------

To stop a timer:

Post Variable Array Fields:
* action: "stop"
* timer_id: 1420259
* stopped_at: ‘2016-04-19 10:50:11’

Response:
{
    "elapsed": 366,
    "entry_id": "8780527",
    "entry_time": 366
}

