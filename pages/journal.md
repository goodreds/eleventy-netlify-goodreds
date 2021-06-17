---
title: "Journal"
metaDescription: This is a sample meta description. If one is not present in your page/post's front matter, the default metadata.desciption will be used instead.
date: "2021-06-16"
permalink: /journal/index.html
eleventyNavigation:
  key: Journal
  order: 5
hero: '/static/img/hero/pencils.jpg'
---

Here are the latest entries.

<table>
    <thead>
        <tr>
            <th>Date</th>
            <th>Title</th>
            <th>Journal</th>
        </tr>
    </thead>
    <tbody>
        {%- for post in collections.journal -%}
        <tr>
            <td>{{ post.date | readableDate }}</td>
            <td><a href="{{ post.url }}">{{ post.data.title }}</a></td>
            <td>{{ post.data.journal }}</td>
        </tr>
        {%- endfor -%}
    </tbody>
</table>
