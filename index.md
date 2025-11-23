---
layout: default
title: Home
---

<div class="bg-gradient-to-br from-blue-50 to-indigo-100 py-20">
    <div class="max-w-4xl mx-auto px-4 text-center">
        <h1 class="text-5xl font-bold text-gray-900 mb-6">
            Hi, I'm Jan
        </h1>
        <p class="text-xl text-gray-700 mb-8">
            Engineer turned Programmer with passion for Rust and Open-Source Analytics.
        </p>
        <p class="text-lg text-gray-600 max-w-2xl mx-auto mb-8">
            Welcome to my personal website. Here you'll find my blog posts, projects, and talks.
            [Add a brief introduction about yourself and what you do]
        </p>
        <div class="flex justify-center gap-4">
            <a href="/blog.html" class="bg-blue-600 text-white px-6 py-3 rounded-lg font-medium hover:bg-blue-700 transition">
                Read My Blog
            </a>
            <a href="/pages/projects.html" class="bg-white text-blue-600 px-6 py-3 rounded-lg font-medium hover:bg-gray-50 transition border border-blue-600">
                View Projects
            </a>
        </div>
    </div>
</div>

<div class="max-w-4xl mx-auto px-4 py-16">
    <h2 class="text-3xl font-bold mb-8">Latest Blog Posts</h2>
    <div class="space-y-6">
        {% for post in site.posts limit:3 %}
        <article class="bg-white p-6 rounded-lg border border-gray-200 hover:shadow-md transition">
            <h3 class="text-2xl font-semibold mb-2">
                <a href="{{ post.url | relative_url }}" class="text-gray-900 hover:text-blue-600 transition">
                    {{ post.title }}
                </a>
            </h3>
            <time class="text-gray-600 text-sm">{{ post.date | date: "%B %d, %Y" }}</time>
            <p class="text-gray-700 mt-3">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
            <a href="{{ post.url | relative_url }}" class="text-blue-600 hover:text-blue-800 font-medium mt-2 inline-block">
                Read more →
            </a>
        </article>
        {% endfor %}
    </div>

    {% if site.posts.size > 3 %}
    <div class="text-center mt-8">
        <a href="/blog.html" class="text-blue-600 hover:text-blue-800 font-medium">
            View all posts →
        </a>
    </div>
    {% endif %}
</div>

<div class="max-w-4xl mx-auto px-4 py-16 bg-gray-50">
    <h2 class="text-3xl font-bold mb-8">Recent Talks</h2>
    <div class="space-y-6">
        {% assign sorted_talks = site.talks | sort: 'date' | reverse %}
        {% for talk in sorted_talks limit:3 %}
        <article class="bg-white p-6 rounded-lg border border-gray-200 hover:shadow-md transition">
            <h3 class="text-2xl font-semibold mb-2">
                <a href="{{ talk.url | relative_url }}" class="text-gray-900 hover:text-blue-600 transition">
                    {{ talk.title }}
                </a>
            </h3>
            <div class="text-gray-600 text-sm mb-3">
                <span class="font-medium">{{ talk.event }}</span>
                <span class="mx-2">•</span>
                <time datetime="{{ talk.date | date_to_xmlschema }}">{{ talk.date | date: "%B %Y" }}</time>
            </div>
            <p class="text-gray-700 mb-3">{{ talk.description }}</p>
            <div class="flex gap-4 text-sm">
                {% if talk.video_url and talk.video_url != "#" %}
                <a href="{{ talk.video_url }}" target="_blank" rel="noopener noreferrer" class="text-blue-600 hover:text-blue-800 font-medium">
                    Watch Video →
                </a>
                {% endif %}
                {% if talk.slides_url and talk.slides_url != "#" %}
                <a href="{{ talk.slides_url }}" target="_blank" rel="noopener noreferrer" class="text-blue-600 hover:text-blue-800 font-medium">
                    View Slides →
                </a>
                {% endif %}
            </div>
        </article>
        {% endfor %}
    </div>

    {% if site.talks.size > 3 %}
    <div class="text-center mt-8">
        <a href="/pages/talks.html" class="text-blue-600 hover:text-blue-800 font-medium">
            View all talks →
        </a>
    </div>
    {% endif %}
</div>
