# Title

## html

```sh
<div class="dashboard">

	<div class="profile">
		<h2>Good Morning Champ!</h2>
		<p>Time to seize the day!</p>

	</div>

	<div class="schedule-table">
		<h2>Weekly Schedule</h2>
		<div class="table-wrap">
			<table>
				<tr>
					<th>Day</th>
					<th>Scheduled Exercise</th>
					<th>Time</th>
				</tr>
				<tr>
					<td>Monday</td>
					<td>Running</td>
					<td>6:00 AM</td>
				</tr>
				<tr>
					<td>Tuesday</td>
					<td>Swimming</td>
					<td>7:00 AM</td>
				</tr>
				<tr>
					<td>Wednesday</td>
					<td>Cycling</td>
					<td>6:30 AM</td>
				</tr>
				<tr>
					<td>Thursday</td>
					<td>Yoga</td>
					<td>6:00 AM</td>
				</tr>
				<tr>
					<td>Friday</td>
					<td>Weight Training</td>
					<td>8:00 AM</td>
				</tr>
			</table>
		</div>
	</div>

	<div class="exercise-table">
		<h2>Last 5 Exercises</h2>
		<div class="table-wrap">
			<table>
				<tr>
					<th>Exercise</th>
					<th>Duration</th>
				</tr>
				<tr>
					<td>Running</td>
					<td>30 min</td>
				</tr>
				<tr>
					<td>Swimming</td>
					<td>45 min</td>
				</tr>
				<tr>
					<td>Cycling</td>
					<td>60 min</td>
				</tr>
				<tr>
					<td>Yoga</td>
					<td>40 min</td>
				</tr>
				<tr>
					<td>Weight Training</td>
					<td>50 min</td>
				</tr>
			</table>
		</div>
	</div>

	<div class="calories">
		<h2>Active Calories</h2>
		<div><strong>Today:</strong> 500</div>
		<div><strong>This Week:</strong> 3500</div>
		<div><strong>This Month:</strong> 14000</div>
	</div>

	<div class="personal-bests">
		<h2>Personal Bests</h2>
		<ul>
			<li>Fastest 5K Run: 22 min</li>
			<li>Heaviest Deadlift: 250 lbs</li>
			<li>Longest Plank: 3 min</li>
		</ul>
	</div>

	<div class="challenges">
		<h2>Challenges</h2>
		<ul>
			<li>30-Day Running Streak</li>
			<li>1000 Pushups in a Month</li>
			<li>Swim 20km in a Month</li>

		</ul>
	</div>

	<div class="activity-feed">
		<h2>Friends Activity</h2>
		<ul>
			<li>Jane just set a new record in cycling: 30 miles!</li>
			<li>Mike completed the 30-Day Running Streak Challenge!</li>
			<li>Anna shared a new workout: 'Hill Sprints Interval'.</li>
		</ul>
	</div>

</div>
```

## css

```sh
/* Neo-Brutalist Style - Because beauty is overrated. */

@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:ital,wght@0,400;0,700;1,400;1,700&display=swap");

*,
*::before,
*::after {
	box-sizing: border-box;
}

::selection {
	background: #333;
	color: #eee;
}

body {
	font-family: "IBM Plex Mono", monospace;
	color: #333;
	margin: 0;
	position: relative;
	line-height: 1.5em;
	font-size: 15px;
	background: repeating-linear-gradient(
		45deg,
		#aaa,
		#aaa 2px,
		#ccc 2px,
		#ccc 6px
	);
	background-attachment: fixed;
}

.dashboard {
	display: grid;
	grid-template-columns: repeat(6, 15.25%);
	grid-gap: 0 1.67%;
	margin: 20px auto;
	padding: 20px;
	border: 2px solid;
	width: 1000px;
	max-width: calc(100% - 40px);
	background: #ddd;
	box-shadow: 1px 1px, 2px 2px, 3px 3px, 4px 4px;
}

.dashboard > div {
	margin-bottom: 20px;
	padding: 15px;
	background-color: #f7f7f7;
	border: 2px solid;
	grid-column: 1 / 7;
	box-shadow: inherit;
}

.dashboard > div:hover {
	background: #fff;
	color: black;
}

.dashboard > div:last-of-type {
	margin-bottom: 5px;
}

.table-wrap {
	max-width: 100%;
	overflow-x: auto;
}

h2 {
	font-size: 1.5em;
	line-height: 1.1em;
	text-transform: uppercase;
	letter-spacing: 0.05em;
	margin-top: 0;
	padding: 5px 10px;
	margin-bottom: 15px;
	border-bottom: 2px solid;
	position: relative;
}

h2::before,
h2::after {
	content: "";
	position: absolute;
	bottom: -2px;
	width: 15px;
	height: 100%;
	left: -15px;
	border: 2px solid;
	border-left: none;
	vertical-align: text-bottom;
}

h2::after {
	left: unset;
	right: -15px;
	border-right: none;
	border-left: 2px solid;
}

table {
	width: 100%;
	border-collapse: collapse;
}

th,
td {
	border: 2px solid #333;
	padding: 8px;
	text-align: left;
}

tr:hover td {
	background: #eee;
}

th {
	background-color: #666;
	color: #fff;
}

ul {
	list-style-type: none;
	padding: 0;
}

li {
	padding: 5px 0;
	border-bottom: 2px solid;
}

.calories div {
	font-size: 1.25em;
	line-height: 1.5em;
	border-bottom: 2px solid;
	padding: 5px 0;
}

.profile {
	text-align: center;
}

.profile h2 {
	font-size: 2em;
	padding-bottom: 10px;
	border: none;
}

.profile p {
	font-size: 1.25em;
	font-style: italic;
	margin-bottom: 10px;
}

.dashboard .activity-feed li {
	font-style: italic;
}

@media (min-width: 767px) {
	.dashboard .schedule-table {
		grid-column: 1 / 4;
	}
	.dashboard .exercise-table {
		grid-column: 4 / 7;
	}
	.dashboard .calories {
		grid-column: 1 / 5;
	}
	.dashboard .personal-bests {
		grid-column: 5 / 7;
	}
	.dashboard .challenges {
		grid-column: 1 / 3;
	}
	.dashboard .activity-feed {
		grid-column: 3 / 7;
	}
	.calories div {
		width: 33.333%;
		float: left;
		display: grid;
		border-left: 2px solid;
		padding-left: 10px;
		margin-left: -2px;
		border-bottom: none;
	}
}

/*Close Button Rules*/

.dashboard .profile button {
	display: none;
}

.dashboard button {
	appearance: none;
	border: inherit;
	color: inherit;
	font-family: arial;
	font-size: 24px;
	line-height: 1.1em;
	width: 1.2em;
	height: 1.2em;
	padding: 0;
	text-align: center;
	float: right;
	z-index: 9;
	position: relative;
	background: #eee;
}

.dashboard button:hover {
	background: #666;
	border-color: #666;
	color: white;
}

@media (min-width: 767px) {
	.profile + .personal-bests + div,
	.profile + .exercise-table + div,
	.schedule-table + div {
		grid-column: 4 / 7 !important;
	}
	.profile + .personal-bests,
	.profile + .exercise-table {
		grid-column: 1 / 4;
	}
	.profile + div + div + .personal-bests,
	.profile + .exercise-table + .calories + div {
		grid-column: 1 / 3;
	}
	.profile + div + div + .personal-bests + div,
	.profile + .exercise-table + .calories + div + div {
		grid-column: 3 / 5;
	}
	.profile + div + div + .personal-bests + div + div,
	.profile + .exercise-table + .calories + div + div + div {
		grid-column: 5 / 7;
	}
}
```

## js

```sh
/* Neo-Brutalist Style - Because beauty is overrated. */

@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:ital,wght@0,400;0,700;1,400;1,700&display=swap");

*,
*::before,
*::after {
	box-sizing: border-box;
}

::selection {
	background: #333;
	color: #eee;
}

body {
	font-family: "IBM Plex Mono", monospace;
	color: #333;
	margin: 0;
	position: relative;
	line-height: 1.5em;
	font-size: 15px;
	background: repeating-linear-gradient(
		45deg,
		#aaa,
		#aaa 2px,
		#ccc 2px,
		#ccc 6px
	);
	background-attachment: fixed;
}

.dashboard {
	display: grid;
	grid-template-columns: repeat(6, 15.25%);
	grid-gap: 0 1.67%;
	margin: 20px auto;
	padding: 20px;
	border: 2px solid;
	width: 1000px;
	max-width: calc(100% - 40px);
	background: #ddd;
	box-shadow: 1px 1px, 2px 2px, 3px 3px, 4px 4px;
}

.dashboard > div {
	margin-bottom: 20px;
	padding: 15px;
	background-color: #f7f7f7;
	border: 2px solid;
	grid-column: 1 / 7;
	box-shadow: inherit;
}

.dashboard > div:hover {
	background: #fff;
	color: black;
}

.dashboard > div:last-of-type {
	margin-bottom: 5px;
}

.table-wrap {
	max-width: 100%;
	overflow-x: auto;
}

h2 {
	font-size: 1.5em;
	line-height: 1.1em;
	text-transform: uppercase;
	letter-spacing: 0.05em;
	margin-top: 0;
	padding: 5px 10px;
	margin-bottom: 15px;
	border-bottom: 2px solid;
	position: relative;
}

h2::before,
h2::after {
	content: "";
	position: absolute;
	bottom: -2px;
	width: 15px;
	height: 100%;
	left: -15px;
	border: 2px solid;
	border-left: none;
	vertical-align: text-bottom;
}

h2::after {
	left: unset;
	right: -15px;
	border-right: none;
	border-left: 2px solid;
}

table {
	width: 100%;
	border-collapse: collapse;
}

th,
td {
	border: 2px solid #333;
	padding: 8px;
	text-align: left;
}

tr:hover td {
	background: #eee;
}

th {
	background-color: #666;
	color: #fff;
}

ul {
	list-style-type: none;
	padding: 0;
}

li {
	padding: 5px 0;
	border-bottom: 2px solid;
}

.calories div {
	font-size: 1.25em;
	line-height: 1.5em;
	border-bottom: 2px solid;
	padding: 5px 0;
}

.profile {
	text-align: center;
}

.profile h2 {
	font-size: 2em;
	padding-bottom: 10px;
	border: none;
}

.profile p {
	font-size: 1.25em;
	font-style: italic;
	margin-bottom: 10px;
}

.dashboard .activity-feed li {
	font-style: italic;
}

@media (min-width: 767px) {
	.dashboard .schedule-table {
		grid-column: 1 / 4;
	}
	.dashboard .exercise-table {
		grid-column: 4 / 7;
	}
	.dashboard .calories {
		grid-column: 1 / 5;
	}
	.dashboard .personal-bests {
		grid-column: 5 / 7;
	}
	.dashboard .challenges {
		grid-column: 1 / 3;
	}
	.dashboard .activity-feed {
		grid-column: 3 / 7;
	}
	.calories div {
		width: 33.333%;
		float: left;
		display: grid;
		border-left: 2px solid;
		padding-left: 10px;
		margin-left: -2px;
		border-bottom: none;
	}
}

/*Close Button Rules*/

.dashboard .profile button {
	display: none;
}

.dashboard button {
	appearance: none;
	border: inherit;
	color: inherit;
	font-family: arial;
	font-size: 24px;
	line-height: 1.1em;
	width: 1.2em;
	height: 1.2em;
	padding: 0;
	text-align: center;
	float: right;
	z-index: 9;
	position: relative;
	background: #eee;
}

.dashboard button:hover {
	background: #666;
	border-color: #666;
	color: white;
}

@media (min-width: 767px) {
	.profile + .personal-bests + div,
	.profile + .exercise-table + div,
	.schedule-table + div {
		grid-column: 4 / 7 !important;
	}
	.profile + .personal-bests,
	.profile + .exercise-table {
		grid-column: 1 / 4;
	}
	.profile + div + div + .personal-bests,
	.profile + .exercise-table + .calories + div {
		grid-column: 1 / 3;
	}
	.profile + div + div + .personal-bests + div,
	.profile + .exercise-table + .calories + div + div {
		grid-column: 3 / 5;
	}
	.profile + div + div + .personal-bests + div + div,
	.profile + .exercise-table + .calories + div + div + div {
		grid-column: 5 / 7;
	}
}
```

