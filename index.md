---
layout: default
title: Home
---

<div class="bg-gradient-to-br from-blue-50 to-indigo-100 py-20">
    <div class="max-w-4xl mx-auto px-4 text-center">
        <img src="{{ '/assets/19823005.png' | relative_url }}"
             alt="Jan Kaul"
             class="w-40 h-40 rounded-full mx-auto mb-8 object-cover border-4 border-white shadow-lg">
        <h1 class="text-5xl font-bold text-gray-900 mb-6">
            Hi, I'm Jan
        </h1>
        <p class="text-xl text-gray-700 mb-8">
            Engineer turned Programmer with passion for Rust and Open-Source Analytics.
        </p>
        <p class="text-lg text-gray-600 max-w-2xl mx-auto mb-8">
            Welcome to my personal website. Here you'll find my blog posts, projects, and talks about open-source analytics, Apache Iceberg, and data engineering.
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

<div class="max-w-4xl mx-auto px-4 py-16 border-b border-gray-200">
    <div class="flex flex-col md:flex-row gap-8 items-start">
        <div class="flex-1">
            <h2 class="text-3xl font-bold mb-4">About Me</h2>
            <div class="prose prose-lg text-gray-700 space-y-4">
                <p>
                    I'm passionate about building efficient data infrastructure and contributing to open-source analytics projects.
                    My work focuses on <strong>Apache Iceberg</strong>, <strong>DataFusion</strong>, and data transformation tools.
                </p>
                <p>
                    With a background in engineering, I've transitioned into software development with a particular interest in
                    <strong>Rust programming</strong> and its applications in high-performance data processing systems. I enjoy
                    speaking at conferences and meetups, sharing insights about materialized views, incremental view maintenance,
                    and modern data engineering practices.
                </p>
            </div>
        </div>
        <div class="md:w-1/3 bg-blue-50 p-6 rounded-lg">
            <h3 class="text-xl font-semibold mb-4">Focus Areas</h3>
            <ul class="space-y-2 text-gray-700">
                <li class="flex items-start">
                    <svg class="w-5 h-5 text-blue-600 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                    </svg>
                    <span>Apache Iceberg</span>
                </li>
                <li class="flex items-start">
                    <svg class="w-5 h-5 text-blue-600 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                    </svg>
                    <span>Rust Programming</span>
                </li>
                <li class="flex items-start">
                    <svg class="w-5 h-5 text-blue-600 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                    </svg>
                    <span>Data Engineering</span>
                </li>
                <li class="flex items-start">
                    <svg class="w-5 h-5 text-blue-600 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                    </svg>
                    <span>Materialized Views</span>
                </li>
                <li class="flex items-start">
                    <svg class="w-5 h-5 text-blue-600 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                    </svg>
                    <span>Open-Source Analytics</span>
                </li>
            </ul>
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
