---
layout: home 
author_profile: true
pubs:
  - author: "Jason Ansel, Marek Olszewski"
    title: "BFTree - Scaling HotStuff to Millions of Validators"
    month: "June"
    year: "2019"
    booktitle: "Whitepaper"
    url: "https://medium.com/celohq/bftree-scaling-hotstuff-to-millions-of-validators-7d6930ee046a"

  - author: "Malavika Samak, Deokhwan Kim, Martin Rinard"
    title: "Synthesizing Replacement Classes"
    month: "January"
    year: "2020"
    booktitle: "47th ACM SIGPLAN Symposium on Principles of Programming Languages (POPL)"
    url: "https://drive.google.com/file/d/184G7NeSGOVaKcO8TpI5p3epqQQarHhwz/view?usp=sharing"
    slides: "https://drive.google.com/file/d/1sH1A_C_KVGIWyDY3TdOFIW7ncm_3jh-n/view?usp=sharing"

---

# Publications

{% for pub in page.pubs %}
{% unless pub.hidden %}
  - {% if pub.url %} [{{pub.title}}]({{pub.url}}).
    {% else %} {{pub.title}}.
    {% endif %}{% if pub.type %}({{pub.type}})
    {% endif %}<br>
    {{pub.author}}.<br>
    {% if pub.type == 'Technical Report' %}{{pub.number}}
    {% endif %}{{pub.booktitle}}{{pub.school}}{{pub.journal}}.<br>
    {% if pub.address %}{{pub.address}}.
    {% endif %} {{pub.month}}, {{pub.year}}. {% if pub.slides %}[Slides]({{pub.slides}}).
    {% endif %}{% if pub.key %}[Bibtex](http://groups.csail.mit.edu/commit/bibtex.cgi?key={{pub.key}}).
    {% endif %}{% if pub.bibtex %}[Bibtex]({{pub.bibtex}}).
    {% endif %}
{% endunless %}
{% endfor %}
