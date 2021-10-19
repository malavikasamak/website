---
layout: home
author_profile: true
pubs:
  - author: "<b>Malavika Samak</b>, Jose Pablo Cambronero, Martin Rinard"
    title: "Searching for Replacement Classes"
    booktitle: "Under Submission"
    url: "https://arxiv.org/pdf/2110.05638.pdf"

  - author: "<b>Malavika Samak</b>, Deokhwan Kim, Martin Rinard"
    title: "Synthesizing Replacement Classes"
    booktitle: "47th ACM SIGPLAN Symposium on Principles of Programming Languages (POPL 2020)"
    url: "https://drive.google.com/file/d/184G7NeSGOVaKcO8TpI5p3epqQQarHhwz/view?usp=sharing"


  - author: "<b>Malavika Samak</b>, Omer Tripp, Murali  Krishna Ramanathan"
    title: "Directed Synthesis of Failing Concurrent Executions"
    booktitle: "Annual Conference on Object-oriented Programming, Systems, Languages, and Applications (OOPSLA 2016)"
    url: "https://drive.google.com/file/d/1b_pmTKNz9ofYbhCWgdHQmct4JQolJftB/view?usp=sharing"

---
<h1> Malavika Samak </h1>
I am a Postdoctoral Associate at [CSAIL, MIT] working with [Prof. Martin Rinard]. 
I received my PhD from [IISc, Bangalore] and was supported 
by a [Google India PhD fellowship]. My research interests are in program 
analysis and software engineering. More specifically:
<li> static and dynamic program analysis </li>
<li> software testing and reliability </li>
<li> code search and replacement </li> 
<li> program synthesis and verification </li>
My long term goal is
to build analyses that can improve developer productivity and software reliability.
I have worked on synthesizing targeted multithreaded tests 
for detecting concurrency bugs in software libraries \([OOPSLA'14], [PLDI'15], [FSE'15], [OOPSLA'16]\), improving the precision
of dynamic analysis for bug detection \([PPoPP'14]\), applying program synthesis 
for optimizing database queries \([SOSP'17]\) and synthesizing adapters to enable 
software library replacement \([POPL'20]\). 
Currently, I am working on efficient search techniques to identify replacement 
Java classes from large codebase collections \([arXiv'21]\).

<h3 style="color:Red;"> I am on the job market this year!</h3>

<h2> Select Publications</h2>
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
    {% endif %}{% if pub.slides %}[Slides]({{pub.slides}}).
    {% endif %}{% if pub.key %}[Bibtex](http://groups.csail.mit.edu/commit/bibtex.cgi?key={{pub.key}}).
    {% endif %}{% if pub.bibtex %}[Bibtex]({{pub.bibtex}}).
    {% endif %}
{% endunless %}
{% endfor %}

<!--[Complete list]-->

[CSAIL, MIT]: https://www.csail.mit.edu/
[Prof. Martin Rinard]: http://people.csail.mit.edu/rinard/
[IISc, Bangalore]: https://iisc.ac.in/
[Google India PhD fellowship]: https://research.google/outreach/phd-fellowship/recipients/?category=2015
[OOPSLA'14]: https://drive.google.com/file/d/1uimZcdYO09fJKL0P-W7dvK39vHr5msG_/view?usp=sharing
[PLDI'15]: https://drive.google.com/file/d/1ptqjFHiVjvlBmnV4zl8hc6EDvRdQ0Mdp/view?usp=sharing
[FSE'15]: https://drive.google.com/file/d/1Fxozt5Wh7q0QQlK1NiUqIvNptRuGKkJu/view?usp=sharing
[POPL'20]: https://drive.google.com/file/d/184G7NeSGOVaKcO8TpI5p3epqQQarHhwz/view?usp=sharing
[OOPSLA'16]: https://drive.google.com/file/d/1b_pmTKNz9ofYbhCWgdHQmct4JQolJftB/view?usp=sharing
[PPoPP'14]: https://drive.google.com/file/d/1O03BO-8kMnEhbXzdVNHV5BLiFgcYggfN/view?usp=sharing
[SOSP'17]:https://drive.google.com/file/d/1i7wwURr--K3JtoM9jqnhQcQkUvL6Ov_J/view?usp=sharing
[arXiv'21]:https://arxiv.org/abs/2110.05638
[Complete list]: /publications/
