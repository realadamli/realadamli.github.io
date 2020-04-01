---
layout: default
---

<!-- Section -->
<!--section>
	<header class="major">
		<h2>Erat lacinia</h2>
	</header>
	<div class="features">
		<article>
			<span class="icon fa-diamond"></span>
			<div class="content">
				<h3>Portitor ullamcorper</h3>
				<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			</div>
		</article>
		<article>
			<span class="icon fa-paper-plane"></span>
			<div class="content">
				<h3>Sapien veroeros</h3>
				<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			</div>
		</article>
		<article>
			<span class="icon fa-rocket"></span>
			<div class="content">
				<h3>Quam lorem ipsum</h3>
				<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			</div>
		</article>
		<article>
			<span class="icon fa-signal"></span>
			<div class="content">
				<h3>Sed magna finibus</h3>
				<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			</div>
		</article>
	</div>
</section>


<!--  <header>
		<h1>Welcome to Koan Trading<br />
		</h1>
		<p>Personal trading and development blog</p>
	</header>
	<p>Koan Trading is a personal trading and development blog. Here, I will be market analysis, trades and trade review, developmental objectivse and progress, educational information, and more. Thanks for taking some time out of your day, I hope you are able to find some value.</p>
	<ul class="actions">
		<li><a href="#" class="button big">Latest Post</a></li>
	</ul>
</div>
<!--  <span class="image object">
	<img src="assets/images/pic10.jpg" alt="" />
</span>-->

<!-- Section -->
<br />
<header class="major">
	<h1>Latest Post</h1>

	<label id="greeting"></label>

<script>
    var myDate = new Date();
    var currentHour = myDate.getHours();

    var msg;

    if (currentHour < 12)
        msg = 'Good Morning';
    else if(currentHour == 12)
	msg = 'Good Noon';
    else if (currentHour >= 12 && currentHour <= 17)
        msg = 'Good Afternoon';
    else if (currentHour >= 17 && currentHour <= 24)
        msg = 'Good Evening';

    document.getElementById('greeting').innerHTML =
        '<b>' + msg + '</b>';
</script>
<!--	<p>Welcome back to Kōan Trading</p>-->
</header>

<div class = "row">
  <div class="6u 12u$(small)">

		<p> {% for post in site.posts limit:1 %}
		<span class="image fit"><img src="{{ post.thumbnail }}" style="width: 100%; max-height: 100%" alt="{{ post.alt }}"/></span>
		{% endfor %}</p>
	</div>
	<div class="6u 12u$(small)">
	{% for post in site.posts limit:1 %}
		<header class ="major">
			<h2>{{ post.title}}</h2>
			<p>{{ post.date | date_to_string }} | {{ post.category }}</p>
			</header>
			{{ post.excerpt | strip_html | strip_newlines | truncate: 300 }} <br />
			<br />

			<ul class="actions">
				<li><a href="{{ post.url }}" class="button big">Read Now</a></li>
			</ul>
	{% endfor %}
	</div>

<section>
<hr class="major" />
<!-- Section -->
<section>
	<header class="major">
		<h2>Recent Posts</h2>
	</header>
	<div class="posts">

		{% for post in site.posts offset:1 limit: 6 %}
			<article>
			<span class="image fit"><img src="{{ post.thumbnail }}" style="width: 100%; max-height: 100%" alt="{{ post.alt }}"/></span>
				<header class = "major">
					<h2>{{ post.title}}</h2>
					<p>{{ post.date | date_to_string }} | {{ post.category }}</p>
					</header>
				{{ post.excerpt | strip_html | strip_newlines | truncate: 156 }} <br/>
<br/>
				<ul class="actions">
					<li><a href="{{ post.url }}" class="button">Read Now</a></li>
				</ul>
			</article>
		{% endfor %}

	<!--	<article>
			<a href="#" class="image"><img src="assets/images/pic01.jpg" alt="" /></a>
			<h3>Interdum aenean</h3>
			<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			<ul class="actions">
				<li><a href="#" class="button">More</a></li>
			</ul>
		</article>
		<article>
			<a href="#" class="image"><img src="assets/images/pic02.jpg" alt="" /></a>
			<h3>Nulla amet dolore</h3>
			<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			<ul class="actions">
				<li><a href="#" class="button">More</a></li>
			</ul>
		</article>
		<article>
			<a href="#" class="image"><img src="assets/images/pic03.jpg" alt="" /></a>
			<h3>Tempus ullamcorper</h3>
			<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			<ul class="actions">
				<li><a href="#" class="button">More</a></li>
			</ul>
		</article>
		<article>
			<a href="#" class="image"><img src="assets/images/pic04.jpg" alt="" /></a>
			<h3>Sed etiam facilis</h3>
			<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			<ul class="actions">
				<li><a href="#" class="button">More</a></li>
			</ul>
		</article>
		<article>
			<a href="#" class="image"><img src="assets/images/pic05.jpg" alt="" /></a>
			<h3>Feugiat lorem aenean</h3>
			<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			<ul class="actions">
				<li><a href="#" class="button">More</a></li>
			</ul>
		</article>
		<article>
			<a href="#" class="image"><img src="assets/images/pic06.jpg" alt="" /></a>
			<h3>Amet varius aliquam</h3>
			<p>Aenean ornare velit lacus, ac varius enim lorem ullamcorper dolore. Proin aliquam facilisis ante interdum. Sed nulla amet lorem feugiat tempus aliquam.</p>
			<ul class="actions">
				<li><a href="#" class="button">More</a></li>
			</ul>
		</article>-->
	</div>
</section>
