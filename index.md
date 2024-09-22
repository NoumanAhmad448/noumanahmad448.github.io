---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
is_homepage: true
---


# Porfolio


{% if site.open_projects %}
## Free Projects
<ul>
{% for pro in site.data.free_projects %}
  <li><a target="_blank" href="{{ site.github_path }}{{pro.repo}}">{{pro.repo}} <strong> {{pro.desc}} </strong> {{pro.emoji}}
    <strong>{{pro.technologies}}</strong>
        <img src = "{{pro.img}}" width ="{{pro.img_w}}" />
    </a>
  </li>
{% endfor %}
</ul>


## Paid Projects
<ul>
{% for pro in site.data.paid_projects %}
  <li><a target="_blank" href="{{ pro.url }}">{{pro.desc}}  {{pro.emoji}}
    <strong>{{pro.technologies}}</strong>
        <img src = "{{pro.img}}" width ="{{pro.img_w}}" />
    </a>
  </li>
{% endfor %}
</ul>

## Our Live Projects
<ul>
{% for pro in site.data.live_projects %}
  <li>
    <a target="_blank" href="{{pro.url}}">
        {{pro.desc}} 
        {{pro.emoji}}
        <strong>
            {{pro.technologies}}
        </strong>
        <img src = "{{pro.img}}" width ="{{pro.img_w}}" />
    </a>
  </li>
{% endfor %}
</ul>
{% endif %}
