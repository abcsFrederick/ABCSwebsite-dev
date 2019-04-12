![](assets/images/Programmer's Corner.png)

The Programmer's Corner, sponsored by the [Bioinformatics User Forum](https://abcsfrederick.info/BUF), is a quarterly meeting of programmers to discuss topics of interest to the group. We usually have 2 or 3 short talks centered around a common topic, followed by discussion.

## Upcoming Programmer's Corner Meetings

<ul>
    {% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
    {% for post in site.posts %}
    {% if post.categories contains "seminars" and post.tags contains "programmers corner" %}
        {% capture posttime %}{{ post.date | date: '%s' }}{% endcapture %}
        {% if posttime > nowunix %}
            <li>
                <a href="{{ site.baseurl }}{{ post.url }}">{{ post.date | date: "%-d %B %Y"}}, {{ post.title }}</a>
            </li>
        {% endif %}
    {% endif %}
    {% endfor %}
</ul>


## Previous Programmer's Corner Meetings

<ul>
    {% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
    {% for post in site.posts %}
    {% if post.categories contains "seminars" and post.tags contains "programmers corner" %}
        {% capture posttime %}{{ post.date | date: '%s' }}{% endcapture %}
        {% if posttime < nowunix %}
            <li>
                <a href="{{ site.baseurl }}{{ post.url }}">{{ post.date | date: "%-d %B %Y"}}, {{ post.title }}</a>
            </li>
        {% endif %}
    {% endif %}
    {% endfor %}
</ul>
