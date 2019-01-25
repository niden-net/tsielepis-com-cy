---
layout: page_blog
language: en
image: /assets/files/news.jpg
title: Careers
permalink: /en/news
---
<div class="blogpostItem clearfix post type-post status-publish format-standard has-post-thumbnail hentry">
    {% for post in site.posts %}
    {% if forloop.index < 3 %}
    <div class="blogItemDate">
        <div class="blogItemDateIn">
            <strong>{{ post.date | date: "%A" }}</strong>
            <br />
            {{ post.date | date: "%B %d, %Y" }}
        </div>
    </div>
    <div class="blogItemBx clearfix">
        <div class="blogThumb">
            <a href="{{ post.url }}">
                <img width="300" 
                     height="300" 
                     src="{{ post.photo }}" 
                     class="attachment-storythumb size-storythumb wp-post-image" 
                     alt="{{ post.title }}" />
            </a>
        </div> 
        <h3 class="postTitle"> 
            <a href="{{ post.url }}">
                {{ post.title }}
            </a>
        </h3>
        <div class="postContent">
            {{ post.excerpt }}
            <a class="readMoreLink" href="{{ post.url }}">Click here to read more.</a>
        </div>
    </div>
    {% endif %}
    {% endfor %}
</div>

<div class="divider2"></div>
<h3 class="title padLeft noBar">
    News Archive
</h3>
<div class="blogpostItem clearfix post type-post status-publish format-standard has-post-thumbnail hentry">
    {% for post in site.posts %}
    {% if forloop.index > 2 %}
    <div class="blogItemDate">
        <div class="blogItemDateIn">
            <strong>{{ post.date | date: "%A" }}</strong>
            <br />
            {{ post.date | date: "%B %d, %Y" }}
        </div>
    </div>
    <div class="blogItemBx clearfix">
        <h3 class="postTitle archiveTitle">
            <a href="{{ post.url }}">
                {{ post.title }}
            </a>
        </h3>
        <div class="postContent">
            {{ post.excerpt }} 
            <a class="readMoreLink" href="{{ post.url }}">
                Click here to read more.
            </a>
        </div>
    </div>
    {% endif %}
    {% endfor %}
</div>
