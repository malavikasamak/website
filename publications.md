---
layout: home 
author_profile: true
pubs:
  - author: "Malavika Samak, Deokhwan Kim, Martin Rinard"
    title: "Synthesizing Replacement Classes"
    month: "January"
    year: "2020"
    booktitle: "47th ACM SIGPLAN Symposium on Principles of Programming Languages (POPL)"
    url: "https://drive.google.com/file/d/184G7NeSGOVaKcO8TpI5p3epqQQarHhwz/view?usp=sharing"
    slides: "https://drive.google.com/file/d/1sH1A_C_KVGIWyDY3TdOFIW7ncm_3jh-n/view?usp=sharing"

  - author: "Matthias Schlaipfer, Kaushik Rajan, Akash Lal, Malavika Samak"
    title: "Optimizing Big-Data Queries Using Program Synthesis"
    month: "October"
    year: "2017"
    booktitle: "26th ACM Symposium on Operating Systems Principles (SOSP)"
    url: "https://drive.google.com/file/d/1i7wwURr--K3JtoM9jqnhQcQkUvL6Ov_J/view?usp=sharing"

  - author: "Malavika Samak, Omer Tripp, Murali  Krishna Ramanathan"
    title: "Directed Synthesis of Failing Concurrent Executions"
    month: "October"
    year: "2016"
    booktitle: "Annual Conference on Object-oriented Programming, Systems, Languages, and Applications (OOPSLA)"
    url: "https://drive.google.com/file/d/1b_pmTKNz9ofYbhCWgdHQmct4JQolJftB/view?usp=sharing"
    slides: "https://drive.google.com/open?id=0B00Hh2TNnne4YThLZlJ6WnExV28"

  - author: "Malavika Samak, Murali  Krishna Ramanathan"
    title: "Synthesizing Tests for Detecting Atomicity Violations"
    month: "September"
    year: "2015"
    booktitle: "10th Joint Meeting of the European Software Engineering Conference and the ACM SIGSOFT Symposium on the Foundations of Software Engineering (FSE)"
    url: "https://drive.google.com/file/d/1Fxozt5Wh7q0QQlK1NiUqIvNptRuGKkJu/view?usp=sharing"
    slides: "https://drive.google.com/file/d/0B00Hh2TNnne4WVdFX3JpZWxtM2s/view?usp=sharing"

  - author: "Malavika Samak, Murali  Krishna Ramanathan, Suresh Jagannathan"
    title: "Synthesizing Racy Tests"
    month: "June"
    year: "2015"
    booktitle: "36th Annual ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI)"
    url: "https://drive.google.com/file/d/1ptqjFHiVjvlBmnV4zl8hc6EDvRdQ0Mdp/view?usp=sharing"
    slides: "https://drive.google.com/file/d/0B50Ds4dSESBaNTBxeDdJQXJ3NlU/view?usp=sharing"

  - author: "Malavika Samak, Murali  Krishna Ramanathan"
    title: "Multithreaded Test Synthesis for Deadlock Detection"
    month: "October"
    year: "2014"
    booktitle: "Annual Conference on Object-Oriented Programming, Systems, Languages, and Applications (OOPSLA)"
    url: "https://drive.google.com/file/d/1uimZcdYO09fJKL0P-W7dvK39vHr5msG_/view?usp=sharing"

  - author: "Malavika Samak, Murali  Krishna Ramanathan"
    title: "Trace Driven Dynamic Deadlock Detection and Reproduction"
    month: "February"
    year: "2014"
    booktitle: "19th ACM SIGPLAN Symposium on Principles and Practice of Parallel Programming (PPoPP)"
    url: "https://drive.google.com/file/d/1O03BO-8kMnEhbXzdVNHV5BLiFgcYggfN/view?usp=sharing"

tool_pubs:
  - author: "Malavika Samak, Murali  Krishna Ramanathan"
    title: "Omen+: A Precise Dynamic Deadlock Detector for Multithreaded Java Libraries"
    month: "November"
    year: "2014"
    booktitle: "22nd ACM SIGSOFT International Symposium on Foundations of Software Engineering (FSE)"

  - author: "Malavika Samak, Murali  Krishna Ramanathan"
    title: "Omen: A Tool for Synthesizing Tests for Deadlock Detection"
    month: "October"
    year: "2014"
    booktitle: "Proceedings of the companion publication of the 2014 ACM SIGPLAN Conference on Systems, Programming, and Applications: Software for Humanity (SPLASH)"
---

<h1> Publications </h1>

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

# Tool Papers
{% for pub in page.tool_pubs %}
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
