# test_tracking
<!DOCTYPE html>
<html>
<head>
	<title>Click Tracking Example with Amplitude</title>
	<script src="https://cdn.amplitude.com/libs/amplitude-7.3.0-min.gz.js"></script>
	<script>
		amplitude.getInstance().init("a46acdaf1fcc731842b7a32fc43389a5");
 
		$(document).ready(function() {
			$('button').click(function() {
				amplitude.getInstance().logEvent('Button Clicked', { 'Button Text': $(this).text() });
			});
		});
	</script>
</head>
<body>
	<h1>Click Tracking Example with Amplitude</h1>
	<p>Click the button below to track a click:</p>
	<button>Click me!</button>
</body>
</html>
