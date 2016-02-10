---
use:
  - docs
title: All Articles
layout: doc
landing_subdirs: true
---

{% for doc in data.docs %}
<a href="{{ doc.url }}">{{ doc.title }}</a><br>
{% endfor %}
