---
theme: ./theme
title: From ES6 to ES.Next - JavaScript features you have to know!
website: lichter.io
handle: TheAlexLichter
favicon: https://lichter.io/img/me@2x.jpg
highlighter: shiki
lineNumbers: true
---

## Catcher (PLAYED)
Oh, so you are a JavaScript (or TypeScript) developer?
Name every feature!

---

<img src="https://i.giphy.com/media/oSYflamt3IEjm/giphy.webp" class="w-screen h-screen absolute top-0 left-0">

<logos-javascript class="absolute text-10xl opacity-75 top-50 left-100"/>

<!--

* JavaScript is constantly evolving
* Introducing new syntax and features regularly
* But how is the process of adding new functionality to the language?
* And which features are easily overlooked but can be very helpful?

-->
---
layout: intro
---

# From ES6 to ES.<span class="text-yellow-400">Next</span>

## JavaScript features you <span class="text-yellow-400">have</span> to know! 

<br><br><br><br>

### Geekle JavaScript Global Summit’22

---

# JavaScript eats the world

<VClicks>

* It can run almost anywhere nowadays
* In the browser
* On the PC/server via Node.js
* Via PaaS/FaaS as e.g. serverless functions
* On the edge (V8 isolates, rarely Node.js itself)

</VClicks>

---

# But how is a new "JavaScript version" created?

<VClicks>

* A new standard every year - most famously **ES6** (also known as **ES2015**)
* Current version: **ES13** or **ES2022**
* Responsibility: ECMA organization, more specific the *TC39* committee
* **E**CMA**S**cript -> **ES**
* Proposals can be submitted at any time and go through up to 5 stages (starting at Stage 0)
* Stage 4 proposals become part of the specification

</VClicks>

---

# Stage 0 - Strawperson 

<VClicks>

* Any discussion, idea or sketch of a proposal that has not been submitted as a "formal" proposal
* Submitted either by a delegate of the TC39 committee or from non-delegates who signed the CLA
* No formal criteria
* "Just input"

</VClicks>

<!--

CLA - Contributors License Agreement for intelectual property rights and stuff

-->

---

# Stage 1 - Proposal

<VClicks>

* has a *Champion*, that...
  * ...is the author or editor of the propsal
  * ...is responsible for the evolution of it through the different stages
  * ...is usually presenting the proposal in TC39 meetings
  * ...is a *member of the TC39 committee*
* does not need a spec text yet
* is more mature and also highlights...
  * ...implementation detail
  * ...high level API
  * ...possible other proposals
  * ...shortcomings and issues

</VClicks>

---

# Stage 2 - Draft

<VClicks>

* Contains everything from Stage 1
* Also has specification text now with major points covered
* Strong commitment for proposal + feature
  * will likely be developed and added to the standard one day

</VClicks>

---

# Stage 3 - Candidate

<VClicks>

* Contains everything from Stage 2
* Has full spec text now
  * Appointed reviewers and all ECMAScript editors have signed off the spec text
* The suggested feature is "complete"
  * No more work to do without experience of usage, implementation and external feedback
  * No changes regarding functionality anymore
* Commonly, implemented via transpiler (Babel) or some browsers already
* Also, TS Support is usual for Stage 3 features

</VClicks>

---

# Stage 4 - Finished

<VClicks>

* Contains everything from Stage 3
* Acceptance tests written for the feature
* Experience thanks to previously shipped implementations
* Will be added to the next revision of the ES standard

</VClicks>

---

# Release of the new standard revisions

<VClicks>

* The ECMAScript Standard is released each year (since 2015)
* Browsers are usually way quicker regarding implementation
* They usually implement ES.Next, so at least all Stage 4 features

</VClicks>

---

* ES?: Tagged template literals
* ES?: `padStart` -> leftpad
* ES?: Modules
* ES6: Destructuring
* ES6: Arrow functions
* ES6: Template Literals
* ES6: Proxy
* ES6: Symbol
* ES8: async/await
* ES6/ES9: Rest/Spread
* ES10: Smooshgate + Array.flat & Array.flatMap
* ES11: globalThis
* ES11: Optional Chaining & Nullish Coalescing
* ES12: Numeric separators
* ES13: Array.at() / String.at() 
* ES14: Array.findLast / Array.findLastIndex
* Proposal: Pipeline Operator
* Proposal: Record & Tuples
* Proposal: Temporal