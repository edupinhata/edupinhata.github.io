---
layout: post
title:  "Google Interview Material"
date:   2024-11-12 10:00 -0300
categories: interview 
---

## Introduction

These days a frient got an oportunity to make a job interview at Google. Since I'm responsible for the technical interview in my company, this is a subject that interests me.
This post is just to put together the preparation material that they asks and probably break it down in further posts.

## Large-Scale System Design Interviews

- Knowledge to solve real-world engineering problems, such as: design policies, processes, procedures, methods, tests, and/or components from the ground up.
- Though process when comming up with a solution.
- Distributing a computation over multiple machines.
- Discuss trade-offs around design decisions.
- Some samples:
  - Traverse a graph;
  - Run-time complexity of graph;
  - Distributes ash table system;
  - Resource estimation with real systems;
  - Big product design picture;
  - Tranlation of an abstract problem to a system;
  - API discussions;
  - Binary trees, cache, MapReduce for loop problems, index, reverse linked-list;
  - Compilers, memory cache, networks.
- Some articles for reference: [Article 1](https://www.hiredintech.com/system-design/), [Article 2](https://github.com/checkcheckzz/system-design-interview)
- Avoid answers that use standard tools: try to create things from scratch.

## Code Review interviews

- In code review, it will be made questions about *style, idiomacy, efficiency, and correctness* of the code in question. Asked to give suggestions on how to improve the code. 
- Tips for a good code review interview:
    - Good self-directed problem solving skills exploring trade offs.
    - Focus open ended problems towards proactive and practical solutions
    - be confident in discussing the *underlying problems* with the code, including issues of performance, complexity, or correctness. Avoid pointing out individual errors line by line and instead focus on the pattern of problem(s) you're seeing in the code.
    - If writing code, show that you had a previous level of mastery and can return to that level quickly;
    - Demonstrate basic knowledge of core language libraries (even if lacking some immediate details)

Aditional areas to review or consider (note that the prep for Coding and code Reivew interviews can overlap)
    - do you think like an engineer? How do you think logically to accomplish a programming task? We're looking for evidence of your past as a string coder;
    - Do you make good choices around which data structures to use for different problems?
    - Can you identify underlying problems and issues of performance in code?
    - Can you identify good style, idiomacy, efficiency, and correctness in code?
    - Do you have basic knowledge of core language libraries?
    - Things we are leninet on: syntax errors, unidiomatic use of the language, library routines, if it takes you more time to get started with solving a problem;
    - To prepare, practice coding exercises similat to [Hackerrank](https://www.hackerrank.com/dashboard) and [Pramp](https://www.pramp.com/#/)
    - Also, the book, ["Cracking the Coding interview"](http://www.crackingthecodinginterview.com/) can be a helpful resource.
    - Yuo can also review the ["Google style guide"](http://google.github.io/styleguide/) for the respective languages as well as know and understand the important parts of the standard libraries for each language:
      - [The Python Standrd Library](https://docs.python.org/3/library/)
      - [Overview (Java Platform SE 8)](https://docs.oracle.com/javase/8/docs/api/index.html)
      - [C++ STL](https://en.cppreference.com/w/)
    - Some books to consider (as applicable):
      - C++: [Effective Modern C++](https://www.oreilly.com/library/view/effective-modern-c/9781491908419/)
      - Java: [Effective Java](https://www.oreilly.com/library/view/effective-java-3rd/9780134686097/)
      - Python: [Fluent Python](https://www.oreilly.com/library/view/fluent-python/9781491946237/) or [Effective Python](https://effectivepython.com/)
      - [Video: Prepare for Coding Interviews](https://www.youtube.com/watch?v=6ZZX9iIgFoo&list=PLllx_3tLoo4c_aR8RKOOnizL5LiUH02YF&index=13&t=0s)

It's a good idea to practice writing code in preparation as well as reading code, and also revieweing the Google style guides for the respective languages.

**General topics to think about:**

- What have you done that demonstrated innovation?
- How did you restructure your team to handle frowth, chagnes to the organization, tracking, procedures? What would you do differently next time?
- What kind of team would you most like to have, serving customer requests, building a single product, building a suite of products, or a combination?
- Was there a time you had a big hit - something with a lot of potential impact - if only you had more developers to work on it? If so, what did you do?
- **Avoid** answers, which involve "use a standard database and do queries against it;" we're not looking for answers involving off-the-shelf products, rather how do you build from scratch?

## Googleyness & Leadership (G&&L)

When you meet with your interviewers, they'll be assessing you on not only your tehcnical skills, but also on how you get work done and collaborate with others. Interviewers will use a mix of behavioral and hypothetical questions to assess:
- Leadership: Be prepared to discuss how you have used your communication and decision-making skills to mobilize others. This might be by stepping up to a leadership role at work or with an organization, or by helping a team succeed even when you weren't officially the leader.
- Googleyness: Share how you work individually and on a team, how you help others, how you navigate ambiguity, and how you push yourself to grow outside of  your confort zone. 

## Some auxiliaty files

- [System Design Interview Prep](./resources/[BR]%20System%20Design%20Interview%20Prep-1.pdf)
- [Eng mrg Prep Material](./resources/[Brazil]%20Eng%20Mrg%20Prep%20Material-1.pdf)
- [G&L Interview Prep Guide](./resources/G&L%20Interview%20Prep%20Guide%20-%20Google%20Docs-1.pdf)
