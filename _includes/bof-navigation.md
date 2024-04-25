
{% assign prev = false %}
{% assign next = false %}
{% assign stillLooking = true %}
{% assign nextOne = false %}


{% comment %}
# this filters all pages with the tag event: and the value
# bof... then sorts them by the value of the tag year.
{% endcomment %}

{% assign items = site.pages | where: "event","bof" | sort: 'year'%}

{% comment %}
# for each of the resulting files, then loop through and generate
# the first/next/prev/last pieces to generate the navigation
# links for the bof traversal based on the current page
{% endcomment %}

{% for c in items %}
  {% comment %}
  # Save the first or the last index/year to avoid
  # generating the prev/next links
  #
  # not needed anymore
  {% if forloop.first == true %}
    {% assign first_yr = c.year %}
  {% elsif forloop.last == true %}
    {% assign last_yr = c.year %}
  {%endif%}
  {% endcomment %}


  {% if stillLooking %}
    {% if c.year == page.year and c.title == page.title %}
      {% assign stillLooking = false %}
      {% assign nextOne = true %}
    {% else %}
      {% assign prev = c %}
      {% assign prevyr = c.year %}
    {% endif %}
  {% elsif nextOne %}
    {% assign next = c %}
    {% assign nextyr = c.year %}
    {% assign nextOne = false %}
  {% endif %}
{% endfor %}


<a name="top" id="top"></a> {% if page.year <= items.first.year %}{% else %} <a href="{{site.baseurl}}{{prev.url}}">← {{prevyr}}</a> &#124; {% endif %}<a href="index.html">Gatherings</a> {% if page.year == items.last.year %}{% else %} &#124; <a href="{{site.baseurl}}{{next.url}}">{{nextyr}} →</a>{% endif %}
