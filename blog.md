---
layout: singlecolumn
title: Blog
permalink: /blog/
---

<h1>Blog</h1>


  <ul class="post-list">
    {% for post in site.posts %}
      <li>        
        <article class="notepad-index-post post row">
            <div class="small-12 medium-3 large-2 columns datetime">
                <span class="notepad-post-meta">
                    <time datetime="{{ post.date | date_to_xmlschema }}">
                        <span class="day">
                            {{ post.date | date: "%d" }}
                        </span>
                        <span class="month-year">
                            {{ post.date | date: "%B %Y" }}
                        </span>
                    </time>
                </span>
            </div>
            <div class="small-12 medium-9 large-10 columns">
                <header class="notepad-post-header">
                    <h3 class="notepad-post-title">
                        <a href="{{ site.url }}{{ post.url }}">
                            {{ post.title }}
                        </a>
                    </h3>
                </header>
                <section class="notepad-post-excerpt">
                    <p>{{ post.content | strip_html | truncatewords:40 }}</p>
                </section>
                Tags:
                <div class="notepad-index-post-tags">
                  {% for tag in post.categories %}<a href="{{ site.url }}/categories/index.html#{{ post.categories | cgi_encode }}" title="Other posts from the {{ tag | capitalize }} category">{{ tag | capitalize }}</a>{% unless forloop.last %}&nbsp;{% endunless %}{% endfor %}                  
                </div>            
            </div>
        </article>
      </li>
    {% endfor %}
  </ul>



<!-- <div class="home">

  <h1 class="page-heading">Posts</h1>

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

  hello :)

  <ul class="docs-list">
    {% for docs in site.docs %}
      <li>
        <span class="post-meta">{{ docs.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ docs.url | prepend: site.baseurl }}">{{ docs.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>  

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
 -->