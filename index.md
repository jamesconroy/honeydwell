---
layout: default
---

{% for post in site.posts limit: 10 %}
  <div class="row-fluid">
    <div class="span12">
      <h2><a href="{{ post.url }}">{{ post.title | truncatewords: 10 | capitalize}}</a></h2>
      <h4>{{ post.date | date: "%b %-d, %Y" }}</h4>
      <h5>{{ post.summary}}</h5>
      <img class="img-responsive" src={{post.picture}} alt={{post.caption}}/>
      <h6>{{post.caption}}</h6>
      <p>
        <a href="{{ post.url }}">Read the Full Post</a>
      </p>
    </div>
  </div>

{% endfor %}

<script type="text/javascript">
/* * * CONFIGURATION VARIABLES: EDIT BEFORE PASTING INTO YOUR WEBPAGE * * */
var disqus_shortname = 'example'; // required: replace example with your forum shortname

/* * * DON'T EDIT BELOW THIS LINE * * */
(function () {
    var s = document.createElement('script'); s.async = true;
    s.type = 'text/javascript';
    s.src = '//' + disqus_shortname + '.disqus.com/count.js';
    (document.getElementsByTagName('HEAD')[0] || document.getElementsByTagName('BODY')[0]).appendChild(s);
}());
</script>
