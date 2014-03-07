Tasks
======

GET /tasks
----------

Return all tasks If you want to get only one specific task you can provide a task_id in get parametr.

Example:
`https://www.timecamp.com/third_party/api/tasks/api_token/a36cabi96bba83f826`
`https://www.timecamp.com/third_party/api/tasks/api_token/a36cabi96bba83f826/task_id/1234`

POST /tasks
----------

Add a new task. To add a task you should have proper permissions.

Example:
`https://www.timecamp.com/third_party/api/tasks/api_token/a36cabi96bba83f826`

Post Fields:
* name: “Task name”
* keywords: “Keword 1, Keyword 2”
* parent_id: 0
* user_ids: ‘123,563,125’ (optional, comma separated)
* role: 1 (optional, by default 1, 1=manager, 3=regular user)
