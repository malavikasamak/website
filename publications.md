---
layout: home 
author_profile: true
pubs:
  - author: "<b>Malavika Samak</b>, Jose Pablo Cambronero, Martin Rinard"
    title: "Searching for Replacement Classes"
    month: "October"
    year: "2021"
    booktitle: "Under submission"
    url: "https://arxiv.org/pdf/2110.05638.pdf"

  - author: "<b>Malavika Samak</b>, Deokhwan Kim, Martin Rinard"
    title: "Synthesizing Replacement Classes"
    month: "January"
    year: "2020"
    booktitle: "47th ACM SIGPLAN Symposium on Principles of Programming Languages (POPL)"
    url: "/documents/samak-popl20.pdf" 
    slides: "/documents/slides/POPL-2020.pdf"

  - author: "Matthias Schlaipfer, Kaushik Rajan, Akash Lal, <b>Malavika Samak</b>"
    title: "Optimizing Big-Data Queries Using Program Synthesis"
    month: "October"
    year: "2017"
    booktitle: "26th ACM Symposium on Operating Systems Principles (SOSP)"
    url: "/documents/sosp17.pdf"

  - author: "<b>Malavika Samak</b>, Omer Tripp, Murali  Krishna Ramanathan"
    title: "Directed Synthesis of Failing Concurrent Executions"
    month: "October"
    year: "2016"
    booktitle: "Annual Conference on Object-oriented Programming, Systems, Languages, and Applications (OOPSLA)"
    url: "/documents/samak-oopsla16.pdf"
    slides: "/documents/slides/Minion.pdf"

  - author: "<b>Malavika Samak</b>, Murali  Krishna Ramanathan"
    title: "Synthesizing Tests for Detecting Atomicity Violations"
    month: "September"
    year: "2015"
    booktitle: "10th Joint Meeting of the European Software Engineering Conference and the ACM SIGSOFT Symposium on the Foundations of Software Engineering (FSE)"
    url: "/documents/samak-fse15.pdf"
    slides: "/documents/slides/FSE-2015.pdf"
    tool: "https://sites.google.com/view/samak-intruder/home"

  - author: "<b>Malavika Samak</b>, Murali  Krishna Ramanathan, Suresh Jagannathan"
    title: "Synthesizing Racy Tests"
    month: "June"
    year: "2015"
    booktitle: "36th Annual ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI)"
    url: "/documents/samak-pldi15.pdf"
    slides: "/documents/slides/PLDI-2015.pdf"
    tool: "https://sites.google.com/view/samak-narada/home"

  - author: "<b>Malavika Samak</b>, Murali  Krishna Ramanathan"
    title: "Multithreaded Test Synthesis for Deadlock Detection"
    month: "October"
    year: "2014"
    booktitle: "Annual Conference on Object-Oriented Programming, Systems, Languages, and Applications (OOPSLA)"
    url: "/documents/samak-ooplsa14.pdf"
    tool: "https://sites.google.com/view/omen-plus/home"

  - author: "<b>Malavika Samak</b>, Murali  Krishna Ramanathan"
    title: "Trace Driven Dynamic Deadlock Detection and Reproduction"
    month: "February"
    year: "2014"
    booktitle: "19th ACM SIGPLAN Symposium on Principles and Practice of Parallel Programming (PPoPP)"
    url: "/documents/samak-ppopp14.pdf"

tool_pubs:
  - author: "<b>Malavika Samak</b>, Murali  Krishna Ramanathan"
    title: "Omen+: A Precise Dynamic Deadlock Detector for Multithreaded Java Libraries"
    month: "November"
    year: "2014"
    booktitle: "22nd ACM SIGSOFT International Symposium on Foundations of Software Engineering (FSE)"

  - author: "<b>Malavika Samak</b>, Murali  Krishna Ramanathan"
    title: "Omen: A Tool for Synthesizing Tests for Deadlock Detection"
    month: "October"
    year: "2014"
    booktitle: "Proceedings of the companion publication of the 2014 ACM SIGPLAN Conference on Systems, Programming, and Applications: Software for Humanity (SPLASH)"
---

<h1> Peer-reviewed Publications </h1>

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
    {% endif %}{% if pub.tool %}[Tool]({{pub.tool}}).
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
