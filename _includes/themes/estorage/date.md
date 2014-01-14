<!-- changing months name to portuguese -->

{% if page.path contains '_posts' %}
{% assign m = page.date | date: "%-m" %}
{{ page.date | date: "%-d" }} de
{% case m %}
{% when '1' %}janeiro
{% when '2' %}fevereiro
{% when '3' %}março
{% when '4' %}abril
{% when '5' %}maio
{% when '6' %}junho
{% when '7' %}júlio
{% when '8' %}agosto
{% when '9' %}setembro
{% when '10' %}outubro
{% when '11' %}novembro
{% when '12' %}dezembro
{% endcase %}de
{{ page.date | date: "%Y" }}
{% else %}
{% assign m = post.date | date: "%-m" %}
{{ post.date | date: "%-d" }} de
{% case m %}
{% when '1' %}janeiro
{% when '2' %}fevereiro
{% when '3' %}março
{% when '4' %}abril
{% when '5' %}maio
{% when '6' %}junho
{% when '7' %}júlio
{% when '8' %}agosto
{% when '9' %}setembro
{% when '10' %}outubro
{% when '11' %}novembro
{% when '12' %}dezembro
{% endcase %}de
{{ post.date | date: "%Y" }}
{% endif %}