---
layout: post
title:  "Course Conclusion: SonarQube SonarCloud - Continuous Inspection and Code Review"
date:   2024-09-05 10:00 -0300
categories: courses 
---

Intruduction of the SonarQube tool. It was not an really deep course, although gave an overview of the tool.

Some of the topics were:

- Instalation and Configuration;
- Sonar Scanner with Maven, Gradle and Ant;
- Integration with IDE
- Cognitive and Cyclomatic complexity
- Quality Gates
- Quality Profiles
- Rules and rule templates

## Notes

### Cyclomatic Complexity vs Cognitive Complexity

These are two ways to identify how complex the code is, therefore how difficult it's to maintain, refactor, understand.

**Cyclomatic Complexity:** works very well for measuring *testability* but not for maintainability. Doesn't give the measure on complexity of the code in human perspective.

**Cognitive Complexity:** 

- Increment when there is a **break** in the **linear flow** of the code.
- Increment when structures that **break** the flow **are nested**.
- **Ignore "shorthand"** structures that readably condense multiple lines of code into one.
- Tells you how many test cases are needed to cover a diven method.

### Rates

- **Maintainability Rate:** It says if the outstanding remediation cost required is a specific percentage of the time already spent into the application.
- **Reliability Rating:** Related with the number of bugs and its severity.
- **Security Rating:** Related with the number of vulnerabilities and its severity.


![Certificate](/images/Certificates/SonarQubeCourse.jpg)