---
title: "Events"
metaDescription: This is a sample meta description. If one is not present in your page/post's front matter, the default metadata.desciption will be used instead.
date: "2021-06-16"
permalink: /events/index.html
eleventyNavigation:
  key: Events
  order: 4
hero: '/static/img/hero/pencils.jpg'
---

Want to hear me play? Here are the upcoming events.

<table>
    <thead>
        <tr>
            <th>Date</th>
            <th>Title</th>
            <th>Location</th>
        </tr>
    </thead>
    <tbody>
        {%- for post in collections.events -%}
        <tr>
            <td>{{ post.date | readableDate }}</td>
            <td><a href="{{ post.url }}">{{ post.data.title }}</a></td>
            <td>{{ post.data.eventLocation }}</td>
        </tr>
        {%- endfor -%}
    </tbody>
</table>
