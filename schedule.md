---
layout: page
title: Schedule
---

<div class="schedule">
	<h1 class="title">{{ page.title }}</h1>

	<p>You are viewing the demo for a <a href="http://github.com/fourkitchens/jekyll-schedule">Jekyll-powered event schedule</a>.</p>
	<p><a href="http://fourkitchens.com/blog/2013/07/10/jekyll-event-schedule">Read more about how it was built</a> or <a href="http://2013.drupalcampaustin.org/schedule/">see a finished, branded version</a>.</p>
	<p>Feel free to use it for your conference!</p>

	<section id="mon" class="day">
		<header>
			<h2>Monday</h2>
			<span data-room="room-1">Room 1</span>
			<span data-room="room-2">Room 2</span>
			<span data-room="room-3">Room 3</span>
		</header>

		{% for post in site.categories.session reversed %}
			{% capture day %}{{ post.date | date: "%A" }}{% endcapture %}
			{% if day == 'Monday' %}
				{% include schedule-day.html %}
			{% endif %}
		{% endfor %}

	</section> <!-- #mon.day -->

	<section id="tues" class="day">
		<header>
			<h2>Tuesday</h2>
			<span data-room="room-1">Room 1</span>
			<span data-room="room-2">Room 2</span>
			<span data-room="room-3">Room 3</span>
		</header>
		{% for post in site.categories.session reversed %}
		{% if post.day == 'Tuesday' %}
			{% include schedule-day.html %}
		{% endif %}
		{% endfor %}
	</section><!-- #tues.day -->

	<section id="tues" class="day">
		<header>
			<h2>Tuesday</h2>
			<span data-room="room-1">Room 1</span>
			<span data-room="room-2">Room 2</span>
			<span data-room="room-3">Room 3</span>
		</header>
		{% for post in site.categories.session reversed %}
		{% if post.day == 'Tuesday' %}
			{% include schedule-day.html %}
		{% endif %}
		{% endfor %}
	</section><!-- #tues.day -->

	<section id="wednes" class="day">
		<header>
			<h2>Wednesday</h2>
			<span data-room="room-1">Room 1</span>
			<span data-room="room-2">Room 2</span>
			<span data-room="room-3">Room 3</span>
		</header>
		{% for post in site.categories.session reversed %}
		{% if post.day == 'Wednesday' %}
			{% include schedule-day.html %}
		{% endif %}
		{% endfor %}
	</section><!-- #wednes.day -->

	<section id="thurs" class="day">
		<header>
			<h2>Thursday</h2>
			<span data-room="room-1">Room 1</span>
			<span data-room="room-2">Room 2</span>
			<span data-room="room-3">Room 3</span>
		</header>
		{% for post in site.categories.session reversed %}
		{% if post.day == 'Thursday' %}
			{% include schedule-day.html %}
		{% endif %}
		{% endfor %}
	</section><!-- #thurs.day -->

	<section id="fri" class="day">
		<header>
			<h2>Friday</h2>
			<span data-room="room-1">Room 1</span>
			<span data-room="room-2">Room 2</span>
			<span data-room="room-3">Room 3</span>
		</header>
		{% for post in site.categories.session reversed %}
		{% if post.day == 'Friday' %}
			{% include schedule-day.html %}
		{% endif %}
		{% endfor %}
	</section><!-- #fri.day -->

</div><!-- .schedule -->
