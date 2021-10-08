---
layout: home 
author_profile: true
---
# Research

I am interested in building systems that enable developers
to maximize the available resources. One such resource that
I have been looking into recently is: code reuse. Enormous amount 
of code has been built in the past few decades and a significant 
chunk is available in the form of binaries and/or source code to the
public. Developers take an active interest in contributing
to open source projects and open sourcing their own projects.
As of 2021, GitHub hosts around [200 million] repositories and 
it is expected to increase over time. To successfully use this 
code, users are going to need tools and techniques to 1) identify
repositories that offer functionality relevant to the user 2) analyze 
the code for possible defects and inefficiencies 3) automatically update
the code.
I have been working on addressing some of the challenges.

<h2> Search </h2>
Software developers must often replace existing components in
their systems to adapt to evolving environments or tooling. While
 traditional code search systems are effective at retrieving components 
 with related functionality, it is much more challenging to
 retrieve components that can be used to directly replace existing
 functionality, as replacements must account for more fundamental 
 program properties such as type compatibility. To address this
 problem, we built ClassFinder, a system which given a query
 class Q, and a search corpus S, returns a ranked subset of classes
 that can replace Q and its functionality. 

 More details on ClassFinder will be available soon!
<h2> Analyze </h2>

 Concurrency bugs can be immensely disruptive and can cause unexpected 
 program behaviors such as deadlocks, atomicity violations, data races, 
 program crashes etc in multi-threaded programs. In some cases, these 
 bugs have manifested in safety critical systems costing human lives. 
 A multi-threaded program may accidentally import a concurrency bug by 
 accessing a third party library that contains such defects. In such cases, 
 the program will need additional synchronization mechanisms to avoid these 
 bugs, which requires a clear understanding of the bugs present in the library. 
 Concrete tests that expose the defects in the library are useful to understand the defects.
 We built a suite of tools that can synthesize multi-threaded tests that 
 expose various concurrency defects. Check out [Omen+], [Narada] and [Intruder]
 which are available for download.

<h2> Replace </h2>
 Manually updating the application to use a different library can be cumbersome and error prone. 
 For example, even when library versions are updated, backward compatibility 
 is not always maintained. Ensuring that the behavior of the application 
 is unchanged can become non-trivial because an existing class in the library can differ
 from the chosen replacement class in the new library across multiple dimensions – 
 internal data representation, signatures of the provided interfaces, or the 
 underlying functionality offered by these interfaces. This motivates the need for a 
 technique that can synthesize an adapter class for a given replacement class so 
 that the synthesized class is equivalent to the existing class. We built Mask
 to address this challenge. Mask employs static analysis, constraint solving and
 sketch based synthesis to construct adapter class, given the original class O and
 replacement R.

 <h2> Released Tools </h2>
  <b>[Omen+]:</b> Generates tests to detect deadlocks in Java classes.
  
  <b>[Narada]:</b> Generates tests to detect data races in Java classes.
  
  <b>[Intruder]:</b> Generates tests to detect atomicity violations.
 
 [Omen+]: https://sites.google.com/view/omen-plus/home
 [Narada]: https://sites.google.com/view/samak-narada/home
 [Intruder]: https://sites.google.com/view/samak-intruder/home
