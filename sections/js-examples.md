JS Examples
====================

Adding computer activities
----------------

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <script src="https://code.jquery.com/jquery-1.10.2.js"></script>
</head>
<body>
<script>

  var api_key = "a36ca9cba8202dd96bba83f";
  var url = "https://www.timecamp.com/third_party/api/activity";
  var post = { 
  	'api_token': api_key,
  	'computer_activities': [
		{
			'application_name': "Internet",
			'start_time': '2016-07-14 12:32:12',
			'end_time': '2016-07-14 12:33:13',
			'window_title': "Internet",
			'website_domain': "yahoo234.com",
			'task_id': "0",
		},
		{
			'application_name': "Internet",
			'start_time': '2016-07-14 12:34:12',
			'end_time': '2016-07-14 12:34:13',
			'window_title': "Internet",
			'website_domain': "yahoo234.com",
			'task_id': "0",
		},
	]
  };
 
  var posting = $.post( url, post, function( data ) {
  	alert("done: " + data);
  });

</script>
</body>
</html>
```
