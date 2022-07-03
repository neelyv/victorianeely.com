---
layout: default
title: "Home"
---

# Victoria Neely

<img class="img-right" src="assets/images/black-cat.png" alt="Black cat" />
Hi, my name is Victoria, and this is where I stash notes about things I'm learning about and projects I'm working on. In my spare time I record audiobook chapters for <a href="https://librivox.org/reader/16022">LibriVox</a> and occasionally play old computer games.

<h2>Articles</h2>

  <ul>
     {% for post in site.posts %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>

<!--
{% for tag in site.tags %}
  <h2>{{ tag[0] }} articles</h2>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
-->

<h2>Projects</h2>

- **"The Story of My Life" by Helen Keller:** A three-part audiobook series available on LibriVox. Part one is <a href="https://librivox.org/the-story-of-my-life-version-3-by-helen-keller/">Helen's autobiography</a>, part two is <a href="https://librivox.org/the-story-of-my-life-part-2-letters-by-helen-keller/">her letters</a>, and part three is <a href="https://librivox.org/the-story-of-my-life-part-3-by-helen-keller/">a supplemental account of her education</a>. For this collaborative project, I recorded Helen's autobiography and letters. For more of my audio work, visit my <a href="https://librivox.org/reader/16022?primary_key=16022&search_category=reader&search_page=1&search_form=get_results">LibriVox reader page</a>.

- **Example landing page:** A <a href="https://neelyv.github.io/landing-page/">landing page</a> I created based on an exercise by The Odin Project. I used HTML and CSS to create a landing page that closely resembles a screenshot of an example website; see the markup on <a href="https://github.com/neelyv/landing-page">GitHub</a>.

<h2>Contact me</h2>

Feel free to drop me a line at <code>&#104;&#101;&#108;&#108;&#111;&#64;&#118;&#105;&#99;&#116;&#111;&#114;&#105;&#97;&#110;&#101;&#101;&#108;&#121;&#46;&#109;&#101;</code>.