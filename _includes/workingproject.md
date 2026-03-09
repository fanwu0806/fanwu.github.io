<h2 id="working project" style="margin: 2px 0px -15px;">Working Project</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.workingproject.main %}

<li>
<div class="pub-row" style="margin-bottom: 40px; max-width: 1000px;">

  {% if link.image %}
  <div style="margin-bottom: 12px;">
    <img src="{{ link.image }}" 
         class="img-fluid z-depth-1" 
         style="width: 100%; border-radius: 10px;">
  </div>
  {% endif %}

  <div class="title" 
       style="font-size: 1.05rem; font-weight: 600; margin-bottom: 6px;">
       {{ link.title }}
  </div>

  {% if link.notes %}
  <div class="note" 
       style="font-size: 0.9rem; line-height: 1.5; color: #444;">
       {{ link.notes }}
  </div>
  {% endif %}

</div>

</li>
<br>

{% endfor %}

</ol>
</div>
