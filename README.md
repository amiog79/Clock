
<!DOCTYPE html>

<html lang="en">

<head>

	<meta charset="UTF-8" />	<meta name="viewport" content=

		"width=device-width,

		initial-scale=1.0" />

	<title>Digital Clock</title>

	<style>

		#clock {

			font-size: 40px;

			width: 260px;

			margin: 35px;

			text-align: center;

			background:yellow;

			color:blue;

			border: 15px solid red;

			border-radius: 20px;

		}

		

	</style>

</head>

<body>

<h1 style="text-align:center; background:black; color:white;">PRADIPTA GHOSH</h1>

<div id="clock"></div>

	<script>

		setInterval(showTime, 1000);

		function showTime() {

			let time = new Date();

			let hour = time.getHours();

			let min = time.getMinutes();

			let sec = time.getSeconds();

			am_pm = "AM";

			if (hour > 12) {

				hour -= 12;

				am_pm = "PM";

			}

			if (hour == 0) {

				hr = 12;

				am_pm = "AM";

			}

			hour = hour < 10 ? "0" + hour : hour;

			min = min < 10 ? "0" + min : min;

			sec = sec < 10 ? "0" + sec : sec;

			let currentTime = hour + ":"

				+ min + ":" + sec + am_pm;

			document.getElementById("clock")

				.innerHTML = currentTime;

		}

		showTime();

	</script>

</body>

</html>
