---
layout: default
title: People

picture-role-groups:
- {roles: [pi, faculty, postdoc], width: 6}
- {roles: [grad, visit], width: 6}

no-picture-role-groups:
- {roles: [alum], width: 6}
---

<section class="people row justify-content-between">
    {% for role-group in page.picture-role-groups %}
        <div class="col-md-{{ role-group.width }}">
            {% for role in role-group.roles %}
                {% include role-people.html role=role image=true %}
            {% endfor %}
        </div>
    {% endfor %}
</section>

<section class="people row justify-content-between">
    {% for role-group in page.no-picture-role-groups %}
        <div class="col-md-{{ role-group.width }}">
            {% for role in role-group.roles %}
                {% include role-people.html role=role image=false %}
            {% endfor %}
        </div>
    {% endfor %}
</section>
