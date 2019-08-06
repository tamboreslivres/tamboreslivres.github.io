---
title: events
header: Calendar of events
layout: page
graphics: foliage
permalink: /events
---
## Tambores Livres schedule
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
