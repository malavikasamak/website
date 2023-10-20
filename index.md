---
layout: home
author_profile: true
pubs:
  - author: "<b>Malavika Samak</b>, Deokhwan Kim, Martin Rinard"
    title: "Synthesizing Replacement Classes"
    booktitle: "ACM SIGPLAN Symposium on Principles of Programming Languages (POPL 2020)"
    url: "/documents/samak-popl20.pdf"


  - author: "<b>Malavika Samak</b>, Omer Tripp, Murali  Krishna Ramanathan"
    title: "Directed Synthesis of Failing Concurrent Executions"
    booktitle: "Annual Conference on Object-oriented Programming, Systems, Languages, and Applications (OOPSLA 2016)"
    url: "/documents/samak-oopsla16.pdf"

  - author: "<b>Malavika Samak</b>, Murali Krishna Ramanathan, Suresh Jagannathan"
    title: "Synthesizing Racy Tests"
    booktitle: "Annual ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI 2015)"
    url: "/documents/samak-pldi15.pdf"
---
<h1> Malavika Samak </h1>
<p align="justify">I am a program analysis engineer at Apple Inc. working towards mitigating security 
vulnerabilities in programs. Before this, I was a 
Postdoctoral Associate at <a href="https://www.csail.mit.edu/">CSAIL, MIT</a>. 
I received my Ph.D. from <a href="https://iisc.ac.in/">IISc, Bangalore</a>, and was supported 
by a <a href="https://research.google/outreach/phd-fellowship/recipients/?category=2015">Google India Ph.D. fellowship</a>. My research interests are in programming
languages and software engineering. More specifically: </p>
<li> static and dynamic program analysis </li>
<li> software testing and reliability </li>
<li> code search and replacement </li> 
<li> program synthesis and verification </li>
<p align="justify">I am interested in designing techniques, tools, and workflows to improve developer productivity
and software reliability. I have designed program analyses that enable developers to discover,
reason, customize, and adapt code to build defect-free software systems.
Specifically, I have worked on synthesizing targeted multithreaded tests 
for detecting concurrency bugs in software libraries (<a href="/documents/samak-ooplsa14.pdf">OOPSLA'14</a>, <a href="/documents/samak-pldi15.pdf">PLDI'15</a>, 
<a href="/documents/samak-fse15.pdf">FSE'15</a>, <a href="/documents/samak-oopsla16.pdf">OOPSLA'16</a>), improving the precision
of dynamic analysis for bug detection (<a href="/documents/samak-ppopp14.pdf">PPoPP'14</a>), applying program synthesis 
for optimizing database queries (<a href="/documents/sosp17.pdf">SOSP'17</a>) and synthesizing adapters to enable 
software library replacement (<a href="/documents/samak-popl20.pdf">POPL'20</a>). I have also worked on efficient search techniques to identify replacement 
Java classes from large codebase collections (<a href="https://arxiv.org/pdf/2110.05638.pdf">arXiv'21</a>). Currently, I am working on mitigating vulnerabilities in 
C++ programs. More details can be found <a href="https://discourse.llvm.org/t/rfc-c-buffer-hardening/65734"> here </a>. </p>


<!--span style="white-space: nowrap;color:Red">I am on the job market this year! <a href="documents/Research_Statement.pdf">Research Statement,</a> <a href="documents/Malavika_CV.pdf">CV</a> 
</span-->


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
