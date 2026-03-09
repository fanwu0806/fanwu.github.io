<h2 id="working project" style="margin: 2px 0px -15px;">Working Project</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.workingproject.main %}

<li>
<div class="pub-row" style="display: flex; align-items: flex-start; margin-bottom: 30px;">
  <div class="col-sm-5 abbr" style="position: relative; padding-right: 20px; padding-left: 15px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 100%; max-width: 100%; border-radius: 8px;">
    {% endif %}
  </div>

  <div class="col-sm-7" style="position: relative; padding-right: 15px; padding-left: 10px;">
    <div class="title" style="font-size: 1.35rem; font-weight: 600; line-height: 1.4; margin-bottom: 10px;">
      {{ link.title }}
    </div>

    {% if link.notes %}
    <div class="note" style="font-size: 1rem; line-height: 1.7; color: #444;">
      {{ link.notes }}
    </div>
    {% endif %}
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
