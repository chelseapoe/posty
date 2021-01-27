---
permalink: "/2"
layout: home
---

<h2>Upcoming topics</h2>

<ul class="list-plain topic_list">
{% for topic in site.data.topics %}
  <li>
    <div class="topic_emoji">{{ topic.emoji }}</div>
    <div class="topic_date">{{ topic.day }}, {{ topic.date }}</div>
    <div class="topic_name">{{ topic.name }}</div>
    <div class="topic_desc">{{ topic.description }}</div>
    <div class="topic_hashtags">{% for ht in topic.hashtags %}#<a class="light" href="https://www.instagram.com/explore/tags/{{ht}}/" target="_blank">{{ht}}</a>&nbsp;&nbsp;{% endfor %}</div>
  </li>
{% endfor %}
</ul>

<h2>Post Inspiration</h2>
<!-- <p>
  <strong>Browse by vertical:</strong><br />
  <a href="/posts#Automotive">Automotive</a> |
  <a href="/posts#Home Services">Home Services</a> |
  <a href="/posts#Activities & Events">Activities & Events</a> |
  <a href="/posts#Pets">Pets</a> |
  <a href="/posts#Health & Wellness">Health & Wellness</a> |
  <a href="/posts#Nightlife">Nightlife</a> |
  <a href="/posts#Professional Services">Professional Services</a> |
  <a href="/posts#Other">Other</a> |
  <a href="/posts#Spas and Salons">Spas and Salons</a> |
  <a href="/posts#Hotel">Hotel</a>
</p> -->

<ul class="post-gallery">
{% for post in site.data.posts limit:8 %}
  <li>
    <img src="{{post.media}}" />
    <div>
    <p class="caption">{{post.caption}}</p>
    <p class="post_type"><a target="_blank" href="https://passport.mainstreethub.com/location/{{post.location}}">Customer {{post.location}}</a> • {{post.vertical}} • {{post.category}}</p>
    </div>
  </li>
{% endfor %}
</ul>
