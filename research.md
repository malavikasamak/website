---
layout: home 
author_profile: true
---

<h1> Research </h1>

My goal is to build analyses that can improve developer productivity and software reliability.

<!--I am interested in building systems that enable developers
to maximize the available resources. One such resource that
I have been looking into recently is: code reuse. Enormous amount 
of code has been built in the past few decades and a significant 
chunk is available in the form of binaries and/or source code to the
public.--> 
<h2> Research Vision </h2>
Developers take an active interest in contributing
to open source projects and open sourcing their own projects.
As of 2021, GitHub hosts around [200 million] repositories and 
it is expected to grow over time. This ideally must lead
to better code re-use, where the functionality offered
by the public code bases is leveraged by the developers and 
are not locally re-implemented. However the challenge is that,
this requires the developer to familiarize themselves with  
code segments that may be of interest and also be able to reason about
its correctness, efficiency and reliability. Manually finding code that are relevant
and then reasoning about their validity is challenging given the magnitude 
of the search space. This may also result in biased use of code, where code developed
by popular organizations/developers are used more than code built by less known entities
due to lack of visibility.

Therefore to improve developer productivity and to level the playground, 
automated techniques that can
1) identify repositories that offer functionality relevant to the user 2) analyze 
the code for possible defects and inefficiencies 3) rank code bases based on their
robustness and efficiency 4) automatically configure programs for migration, can be
useful. A framework that can deliver such features can not only improve the overall code reuse
program reliability but also democratize the entire process.

I have been working towards realizing some of these goals.

<div class="pad">
<h2> Search </h2>
Software developers must often replace existing components in
their systems to adapt to evolving environments or tooling. While
 traditional code search systems are effective at retrieving components 
 with related functionality, it is much more challenging to
 retrieve components that can be used to directly replace existing
 functionality, as replacements must account for more fundamental 
 program properties such as type compatibility. To address this
 problem, I built ClassFinder, a system which given a query
 class Q, and a search corpus S, returns a ranked subset of classes
 that can replace Q and its functionality. The tool has shown promising 
 results and is able to find replacement classes from a search corpus 
 containing ~600 thousand open source Java classes.

 More details on ClassFinder will be available soon!
<h2> Analyze </h2>

 Analyzing third party code imported by a program for software bugs, 
 memory bloats, execution bottle necks, security threats is important. 
 It enables the developer to understand if their program may have
 accidentally imported defects and enables them to address the defect. I have
 worked on building analyses, that can expose concurrency bugs in third 
 party libraries.
 Concurrency bugs can be immensely disruptive and can cause unexpected 
 program behaviors such as deadlocks, atomicity violations, data races, 
 program crashes etc in multi-threaded programs. In some cases, these 
 bugs have manifested in safety critical systems costing human lives. 
 A multi-threaded program may accidentally import a concurrency bug by 
 accessing a third party library that contains such defects. In such cases, 
 the program will need additional synchronization mechanisms to avoid these 
 bugs, which requires a clear understanding of the bugs present in the library. 
 Concrete tests that expose the defects in the library are useful to understand the defects.
 I built a suite of tools that can synthesize multi-threaded tests that 
 expose various concurrency defects. Check out <a href="https://sites.google.com/view/omen-plus/home">Omen+</a> 
 (<a href="https://drive.google.com/file/d/1uimZcdYO09fJKL0P-W7dvK39vHr5msG_/view?usp=sharing">OOPSLA'14</a>), 
 <a href="https://sites.google.com/view/samak-narada/home">Narada</a>
 (<a href="https://drive.google.com/file/d/1ptqjFHiVjvlBmnV4zl8hc6EDvRdQ0Mdp/view?usp=sharing">PLDI'15</a>), 
 <a href="https://sites.google.com/view/samak-intruder/home">Intruder </a> 
 (<a href="https://drive.google.com/file/d/1Fxozt5Wh7q0QQlK1NiUqIvNptRuGKkJu/view?usp=sharing">FSE'15</a>) 
 and Minion (<a href="https://drive.google.com/file/d/1b_pmTKNz9ofYbhCWgdHQmct4JQolJftB/view?usp=sharing">OOPSLA'16</a>) for more details.
<h2> Replace </h2>
 Manually updating the application to use a different library can be cumbersome and error prone. 
 For example, even when library versions are updated, backward compatibility 
 is not always maintained. Ensuring that the behavior of the application 
 is unchanged can become non-trivial because an existing class in the library can differ
 from the chosen replacement class in the new library across multiple dimensions – 
 internal data representation, signatures of the provided interfaces, or the 
 underlying functionality offered by these interfaces. This motivates the need for a 
 technique that can synthesize an adapter class for a given replacement class so 
 that the synthesized class is equivalent to the existing class. I built MASK 
 (<a href="https://drive.google.com/file/d/184G7NeSGOVaKcO8TpI5p3epqQQarHhwz/view?usp=sharing">POPL'20</a>)
 to address this challenge. Mask employs static analysis, constraint solving and
 sketch based synthesis to construct adapter class, given the original class O and
 replacement R.
 </div>
 <h2> Released Tools </h2>
  <b>[Omen+]:</b> Generates tests to detect deadlocks in Java classes.
  
  <b>[Narada]:</b> Generates tests to detect data races in Java classes.
  
  <b>[Intruder]:</b> Generates tests to detect atomicity violations.
 
 [Omen+]: https://sites.google.com/view/omen-plus/home
 [Narada]: https://sites.google.com/view/samak-narada/home
 [Intruder]: https://sites.google.com/view/samak-intruder/home
 [200 million]: https://github.com/about
 [OOPSLA'14]: https://drive.google.com/file/d/1uimZcdYO09fJKL0P-W7dvK39vHr5msG_/view?usp=sharing
 [PLDI'15]: https://drive.google.com/file/d/1ptqjFHiVjvlBmnV4zl8hc6EDvRdQ0Mdp/view?usp=sharing
 [FSE'15]: https://drive.google.com/file/d/1Fxozt5Wh7q0QQlK1NiUqIvNptRuGKkJu/view?usp=sharing
 [POPL'20]: https://drive.google.com/file/d/184G7NeSGOVaKcO8TpI5p3epqQQarHhwz/view?usp=sharing
