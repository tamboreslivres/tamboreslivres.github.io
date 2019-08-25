---
title: events
header: Calendar of events
layout: page
graphics: foliage
permalink: /events
---
Thank you to all who joined us at Notting Hill Carnival 2019 to celebrate the spirit of Brazilian culture, whilst raising awareness of the social and environmental issues facing Brazil today. It was an amazing day.

We have lots more planned, from fundraising events to education workshops. Please check back soon to find out more.

{% for event in site.data.future-events %}
<span class="date" value="{{event.date}}">**{{event.date | date: '%d %B %Y'}}** — **{{event.name}}** — *{{event.location}}* {% if event.map %} <a class="mx-2" href="{{event.map}}" target="_blank"><i class="fas fa-map-marked-alt"></i></a>{% endif%}</span>
{% endfor %}

# PAST EVENTS

## Tambores Livres Notting Hill Carnival schedule
{% for event in site.data.events %}
<span class="date" value="{{event.date}}">**{{event.date | date: '%d %B %Y'}}** — **{{event.name}}** — *{{event.location}}* {% if event.map %} <a class="mx-2" href="{{event.map}}" target="_blank"><i class="fas fa-map-marked-alt"></i></a>{% endif%}</span>
{% endfor %}
*Address for <u>Maxilla</u>: Maxilla Hall Social Club, 2 Maxilla Walk, W10 6SW, Hall under the A40 highway, Tube: Latimer Road or Ladbroke Grove
<hr class="my-4"/>

## Mestre Chacon’s schedule
{% for event in site.data.chacon-events %}
<span class="date" value="{{event.date}}">**{{event.date | date: '%d %B %Y'}}** — **{{event.name}}** — *{{event.location}}*</span>
{% endfor %}



<script>
function dimDate() {
    var today = new Date();
    $('.date').toArray().forEach(d => {
            date = d.getAttribute("value")
            date = new Date(date)
            console.log(today, date, today > date)
            if (date < today) {
                d.className +=' text-muted'
            }
    })
}
$('document').ready(function() {
    dimDate()
})
</script>
