---
layout: default
title: Event Calendar
permalink: /calendar
header:
  teaser: "/assets/images/pages/calendar/utah-esports-calendar.png"
---

<script src="{{ '/assets/js/moment.min.js' | relative_url }}"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/fullcalendar/3.9.0/fullcalendar.min.js"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/fullcalendar/3.9.0/fullcalendar.min.css">
<link rel="stylesheet" media="print" href="https://cdnjs.cloudflare.com/ajax/libs/fullcalendar/3.9.0/fullcalendar.print.min.css">

<script>
  (function ( $ ) { 
    $(document).ready(function() {
      var w = window.innerWidth;
      $.noConflict();
      $('#calendar').fullCalendar({
        header: {
          left: 'month, listWeek',
          center: 'title',
          right: 'today,prev,next',
        },
        buttonText: {
          month: 'Month',
          listWeek: 'Week'
        },
        defaultView: w < 767 ? 'listWeek' : 'month',
        events:'/calendar-data'
      });
    });
  }( jQuery ));
</script>

<!--
{% for event in site.events %}
{{event.title}} {{event.event_date}}<br/>
{% endfor %}
-->
<div id="calendar"></div>

<style>
  #calendar {
    max-width: 1200px;
    margin: auto;
    padding: 0 30px;
  }
</style>
