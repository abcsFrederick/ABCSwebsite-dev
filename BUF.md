<div>
<p style="float: left;"><img src="assets/images/BUF Logo_trans.png" height="200px"></p>
</div>

# Bioinformatics User Forum

The Bioinformatics User Forum is a place to build the bioinformatics community within the NCI and Frederick National Laboratory as well as among our collaborators at NIH, Ft Detrick and beyond. Anyone interested in the bioinformatics challenges in these communities is welcome to join us (search for "Bioinformatics-User-Forum" at [list.nih.gov](https://list.nih.gov) to sign up for our list serve).

Check out our [Statistics for Lunch](Stats4Lunch) and [Programmer's Corner](ProgrammersCorner) series for additional upcoming events and recordings.

## Upcoming BUF Meetings

<ul>
    {% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
    {% for post in site.posts %}
    {% if post.categories contains "seminars" and post.tags contains "BUF" %}
    {% unless post.tags contains "statistics for lunch" or post.tags contains "programmers corner" %}
        {% capture posttime %}{{ post.date | date: '%s' }}{% endcapture %}
        {% if posttime > nowunix %}
            <li>
                <a href="{{ site.baseurl }}{{ post.url }}">{{ post.date | date: "%-d %B %Y"}}, {{ post.title }}</a>
            </li>
        {% endif %}
    {% endunless %}
    {% endif %}
    {% endfor %}
</ul>


## Previous BUF Meetings

<ul>
    {% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
    {% for post in site.posts %}
    {% if post.categories contains "seminars" and post.tags contains "BUF" %}
    {% unless post.tags contains "statistics for lunch" or post.tags contains "programmers corner" %}
        {% capture posttime %}{{ post.date | date: '%s' }}{% endcapture %}
        {% if posttime < nowunix %}
            <li>
                <a href="{{ site.baseurl }}{{ post.url }}">{{ post.date | date: "%-d %B %Y"}}, {{ post.title }}</a>
            </li>
        {% endif %}
    {% endunless %}
    {% endif %}
    {% endfor %}
</ul>
