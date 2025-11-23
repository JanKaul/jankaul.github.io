---
layout: default
title: Talks
description: Presentations and speaking engagements
permalink: /pages/talks.html
---

<div class="max-w-4xl mx-auto px-4 py-12">
    <header class="mb-12">
        <h1 class="text-4xl font-bold mb-4">Talks & Presentations</h1>
        <p class="text-xl text-gray-600">Speaking engagements and conference presentations</p>
    </header>

    {% assign sorted_talks = site.talks | sort: 'date' | reverse %}

    {% if sorted_talks.size > 0 %}
    <div class="space-y-8">
        {% for talk in sorted_talks %}
        <article class="bg-white p-6 rounded-lg border border-gray-200 hover:shadow-md transition">
            <h2 class="text-2xl font-semibold mb-3">
                <a href="{{ talk.url | relative_url }}" class="text-gray-900 hover:text-blue-600 transition">
                    {{ talk.title }}
                </a>
            </h2>

            <div class="text-gray-600 mb-4">
                <div class="flex flex-wrap gap-x-4 gap-y-2">
                    <div>
                        <span class="font-semibold">Event:</span> {{ talk.event }}
                    </div>
                    <div>
                        <span class="font-semibold">Date:</span>
                        <time datetime="{{ talk.date | date_to_xmlschema }}">{{ talk.date | date: "%B %Y" }}</time>
                    </div>
                </div>
            </div>

            <p class="text-gray-700 mb-4">{{ talk.description }}</p>

            <div class="flex flex-wrap gap-4">
                {% if talk.slides_url and talk.slides_url != "#" %}
                <a href="{{ talk.slides_url }}" target="_blank" rel="noopener noreferrer"
                   class="inline-flex items-center text-blue-600 hover:text-blue-800 font-medium transition">
                    <svg class="w-4 h-4 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/>
                    </svg>
                    Slides
                </a>
                {% endif %}
                {% if talk.video_url and talk.video_url != "#" %}
                <a href="{{ talk.video_url }}" target="_blank" rel="noopener noreferrer"
                   class="inline-flex items-center text-blue-600 hover:text-blue-800 font-medium transition">
                    <svg class="w-4 h-4 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"/>
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/>
                    </svg>
                    Video
                </a>
                {% endif %}
                {% if talk.code_url and talk.code_url != "#" %}
                <a href="{{ talk.code_url }}" target="_blank" rel="noopener noreferrer"
                   class="inline-flex items-center text-blue-600 hover:text-blue-800 font-medium transition">
                    <svg class="w-4 h-4 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"/>
                    </svg>
                    Code
                </a>
                {% endif %}
            </div>
        </article>
        {% endfor %}
    </div>
    {% else %}
    <div class="bg-gray-50 p-8 rounded-lg text-center">
        <p class="text-gray-600 text-lg">No talks yet. Check back soon!</p>
    </div>
    {% endif %}
</div>


